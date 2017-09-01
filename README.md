# Git commands cheatsheet
Bundle of useful git commands


##### Squashing commits
  - ```git rebase -i HEAD~2``` (HEAD~2 means include last 2 commits from HEAD)
  - ```git push -f origin branch_name```

##### Pull hard
Reset local branch to remote hard

  - ```git fetch --all```
  - ```git reset --hard origin/master```
  - or ```git reset --hard origin/<branch_name>```

##### Reverting a commit
  - ```git revert <commit-hash>```
  - ```git push -f origin <branch_name>```

##### Git re-create branch from local (delete and push anew)
  - ```git push --delete origin <branch_name>```   (followed by) 
  - ```git push origin HEAD```

##### Cherry picking
Pick commit and add to current branch. In this example, add commit to master

  - ```git checkout master```
  - ```git cherry-pick <commit-hash>```

##### Rename branch
  - ```git branch -m <oldname> <newname>```

##### Tagging

  - existing commit
    - ```git tag -a <tag_name> <commit_sha> -m "a commit message"```
    - ```git push origin <tag_name>```
    
  - creating tagged commit
     - ```git tag -a <tag_name> -m "<message>"```
     - ```git push origin <tag_name>```
