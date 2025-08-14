# Github !

### Push this directory (repo) to GitHub with all updates

- make sure you’re inside the repo.

```sh
git add .
git commit -m "Updated project"
git pull origin main --rebase
git push origin main

```
- If it’s a new repo not yet connected to GitHub:

```sh
git init
git branch -M main
git remote add origin https://github.com/USERNAME/REPO.git
git add .
git commit -m "Initial commit"
git push -u origin main


#If you deleted files locally and want GitHub to also delete them:
git add -u && git commit -m "remove deleted files" && git push

#Check Ker Kya hua
git status

```

- Quick Update Alias (One Command Push)

```sh
#Make this alias once:
git config --global alias.quick '!git add . && git commit -m "update" && git pull --rebase && git push'

#Then forever after, just run:
git quick
```


#### Clone Your Repo Anywhere

```sh
git clone https://github.com/USERNAME/REPO.git
cd USERNAME/
```
