<details><summary>**Setup bride Windows to WSL**</summary>
<code>
$wsl2_ip = wsl hostname -I | % { $_.Trim() }
$windows_ip = (Test-Connection -ComputerName (hostname) -Count 1).IPV4Address.IPAddressToString
$port = 8080
New-NetFirewallRule -DisplayName "WSL2 Web Server (Port 8080)" -Direction Inbound  -LocalPort $port -Action Allow -Protocol TCP
netsh interface portproxy add v4tov4 listenport=$port listenaddress=$windows_ip connectport=80 connectaddress=$wsl2_ip


#windows:
netsh interface portproxy show all

#wsl:
ip addr show eth0

sudo ss -tuln

ip addr show eth0 | grep -oP '(?<=inet\s)\d+(\.\d+){3}'

sudo nano /etc/ssh/sshd_config

PermitRootLogin no
PasswordAuthentication yes
AllowUsers username
ListenAddress 0.0.0.0

#Windows bride to WSL
netsh interface portproxy add v4tov4 listenaddress=<ip_windows> listenport=2222 connectaddress=<ip_wsl> connectport=22
</div>
</details>

