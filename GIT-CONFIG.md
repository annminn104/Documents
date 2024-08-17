```git config --global --edit

git config core.eol lf
git config core.autocrlf input

# Copy files from the index to the working tree
git checkout-index --force --all

# If above line doesn't work, delete all cached files and reset.
git rm --cached -r .
git reset --hard
```
