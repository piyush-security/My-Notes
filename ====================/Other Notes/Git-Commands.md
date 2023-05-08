- - -
#### Push local repo to remote ( existing ) : 
```sh
git init
git add <folder1> <folder2> <etc.>
git commit -m "Your message about the commit"
git remote add origin https://github.com/yourUsername/yourRepository.git
git push -u origin master
git push -f origin master
git push origin master
```

- - -
#### Change the main repo to master ( as default ) : 

```sh
# Checking : 
git branch
git branch -v
git branch --merged
git branch --no-merged
# Move from main to master.
git branch --move main master
git push --set-upstream origin master
# now check again : 
git branch --all
# delete the main branch now : 
git push origin --delete main
git push origin master
```

 - - -
```sh
git remote -v
git remote rm origin
git remote set-url origin https://pratik@bitbucket.org/pratik/demoapp.git
git push -f origin master
```