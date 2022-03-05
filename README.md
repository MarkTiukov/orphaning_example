# Fix commits to main branch
Imagine, you have made several commits on branch `main`, like in this repository instead of `dev` with following pull-request. To fix this, do following
```bash
git checkout --orphan dev # create an orphan branch 
git commit -m "main copy" # copying all files from 'main'
git push origin dev # save your changes in remote repository
# now we clear main
git checkout main
git reset --hard ${sha-of-first-commit} # if you want to rollback to your first commit
git push # to save your changes in 'main' branch
```
Good luck fixing :)

