Git command list (self-documentation)
https://git-scm.com/doc
_____________________________________________________________
git config --global user.name 'Saul Goodman'
git config --global user.email 'saulgoodman@bettercallsaul.com'
_____________________________________________________________

All about logs:
git log => show commit history
git log --stat => history with statistic data
git log --graph --oneline {BRANCH_NAME} => show all commits in one line with graphics
git log -n5 => show last five commits
_____________________________________________________________

Main:
git diff => show difference between commits, commit and working directory
git clone => option for clone whole repository
git config --global color.ui auto => different color for data
git checkout => switch between branches or restore working tree files
git checkout -b {NEW_BRANCH_NAME} - create new branch from current commits
_____________________________________________________________

Committing me softly:
git status => show changes in current working tree
git add => add files to Staging Area (intermediate zone between local and web)
git rm => delete file from Staging Area
git reset => remove files from staging area
git commit => commit to repository (shorthand git commit -m 'Commit message')
_____________________________________________________________

Branches and etc.:
git branch => show all current branches, create or delete
git branch -a => show all branches, even not synced yet
git branch -d {BRANCH_NAME} => delete branch (after successful merge)
git branch -D {BRANCH_NAME} => delete dead-end branch
git merge {NAME_1} {NAME_2} => Join two branches in one (all development history together), {NAME_1} into {NAME_2}
    1. git checkout {BRANCH_1}
    2. git merge {BRANCH_1} {BRANCH_2} (or git merge {BRANCH_2}
git show => show a lot of objects (blobs, trees, commits)
git show {COMMIT_ID} => compare commit with ancestors
_____________________________________________________________

git merge --abort => abort the current conflict process
git remote => manage repositories on server side, they have names
git remote add origin {URL} - add new remote for the repository
git remote -v => show remote url after name

git push origin {MASTER} => update remote refs using local refs
git pull origin {MASTER} => fetch from and integrate with another repository
_____________________________________________________________

git fetch => download objects and refs from another repository
git pull origin master === git fetch origin
                           git merge master origin/master

git log origin/master => check remote repositories logs
git diff origin/master master => check diff between local and remote repositories
git merge master origin/master => merge twe repositories (original local and remote)
_____________________________________________________________

Example:
    1. git fetch origin
    2. git merge master origin/master
    // or git pull origin master)
    3. FIX POSSIBLE MERGE CONFLICTS
    4. git status
    5. git add .
    6. git commit -m 'Commit name'
    7. git push

_____________________________________________________________

git remote -v
git remote add upstream git@github.com:YerzhanBetov/***.git
git remote -v
git pull upstream develop
git branch -a
