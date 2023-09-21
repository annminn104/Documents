# How to setup next.js app on nginx with letsencrypt
> next.js, nginx, reverse-proxy, ssl

### 1. Install nginx and letsencrypt
```bash
$ sudo apt-get update
$ sudo apt-get install nginx letsencrypt
```
#### Also enable nginx in ufw
```bash
# after installing nginx!
$ sudo ufw allow 'Nginx Full'
```

### 2. Edit our default nginx site file
```bash
$ sudo vim /etc/nginx/sites-available/default
```
##### Content
```
# *q is our domain
server {
  listen 80 default_server;
  listen [::]:80 default_server;

  root /var/www/html;
  index index.html index.htm index.nginx-debian.html;

  server_name q*;

  location / {
    try_files $uri $uri/ =404;
  }
  
  # for letsencrypt
  location ~ /.well-known {
    allow all;
  }
}
```
#### Restart nginx
```bash
$ sudo nginx -t # check syntax errors
$ sudo systemctl restart nginx
```

### 3. Setup letsencrypt
```bash
# *q is our domain
$ sudo letsencrypt certonly -a webroot --webroot-path=/var/www/html -d *q -d www.q*
```

#### Generate Strong DH Group
```bash
$ sudo openssl dhparam -dsaparam -out /etc/ssl/certs/dhparam.pem 2048
```

#### Create nginx config file with Strong Encryption Settings
```bash
$ sudo vim /etc/nginx/snippets/ssl-params.conf
```
##### Content
```
ssl_protocols TLSv1.3; 
ssl_prefer_server_ciphers on;
ssl_ciphers "EECDH+AESGCM:EDH+AESGCM:AES256+EECDH:AES256+EDH";
ssl_ecdh_curve secp384r1;
ssl_session_cache shared:SSL:10m;
ssl_session_tickets off;
ssl_stapling on;
ssl_stapling_verify on;

resolver 8.8.8.8 8.8.4.4 valid=300s;
resolver_timeout 5s;

add_header Strict-Transport-Security "max-age=63072000; includeSubdomains";
add_header X-Frame-Options DENY;
add_header X-Content-Type-Options nosniff;

ssl_dhparam /etc/ssl/certs/dhparam.pem;
```

#### Edit our nginx file
```
# *q is our domain

# redirect http to https
server {
  listen 80 default_server;
  listen [::]:80 default_server;
  server_name *q www.*q;
  return 301 https://$server_name$request_uri;
}

server {
  # listen on *:443 -> ssl; instead of *:80
  listen 443 ssl http2 default_server;
  listen [::]:443 ssl http2 default_server;

  server_name q*;
  
  ssl_certificate /etc/letsencrypt/live/example.com/fullchain.pem;
  ssl_certificate_key /etc/letsencrypt/live/example.com/privkey.pem;
  include snippets/ssl-params.conf;

  location / {
    # reverse proxy for next server
    proxy_pass http://localhost:3000;
    proxy_http_version 1.1;
    proxy_set_header Upgrade $http_upgrade;
    proxy_set_header Connection 'upgrade';
    proxy_set_header Host $host;
    proxy_cache_bypass $http_upgrade;
  
    # we need to remove this 404 handling
    # because next's _next folder and own handling
    # try_files $uri $uri/ =404;
  }
  
  location ~ /.well-known {
    allow all;
  }
}
```

#### Restart nginx again
```bash
$ sudo systemctl restart nginx
```

### 4. Setup next.js app
```bash
$ yarn build # build our app for production (npm build script: next build)
$ yarn global add pm2 # install pm2 to keep next app alive forever*

# run start/stop
$ pm2 start npm --name "next" -- start # start next app (npm start script: next start)
$ pm2 stop next # for stopping app
```

# We are done
Now you have next.js app up and running on nginx reverse proxy with ssl!


server {
  server_name   <domain_name>;

  location / {
    proxy_pass             http://127.0.0.1:<PORT>;
    proxy_read_timeout     60;
    proxy_connect_timeout  60;
    proxy_redirect         off;

    # Allow the use of websockets
    proxy_http_version 1.1;
    proxy_set_header Upgrade $http_upgrade;
    proxy_set_header Connection 'upgrade';
    proxy_set_header Host $host;
    proxy_cache_bypass $http_upgrade;
  }
  
  location /_next/static {
        add_header Cache-Control "public, max-age=3600, immutable";
        proxy_pass http://127.0.0.1:<PORT>/_next/static;
  }

}
