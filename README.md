# Fix commits to main branch
Imagine, you have made several commits on branch `main`, like in this repository instead of `dev` with following pull-request. To fix this, do following
``` Bash
git checkout --orphan dev # create an orphan branch 
# any initial commit for this new orphan branch
git rebase main # remove all commits from 'main' and place'em into 'dev'
git push # save your changes in remote repository
```
Good luck fixing :)

