# git

## Configuration
Useful and recommended variables for .gitconfig

| *variable* | *recommended value* | *link* |
| ---------- | ------- | ------ |
`core.autocrlf` | `true` | [core.autocrlf](https://git-scm.com/docs/git-config#Documentation/git-config.txt-coreautocrlf)
`pull.rebase` | `true` | [pull.rebase](https://git-scm.com/docs/git-config#Documentation/git-config.txt-pullrebase)
`push.followTags` | `true` | [push.followTags](https://git-scm.com/docs/git-config#Documentation/git-config.txt-pushfollowTags)

### Aliases
| *alias* | *command* |
| ------- | --------- |
`a` | `add`
`ap` | `add --patch`
`ci` | `commit`
`cim` | `commit -m`
`cia` | `commit --amend`
`cian` | `commit --amend --no-edit`
`co` | `checkout`
`d` | `diff`
`dw` | `diff --word-diff`
`ds` | `diff --staged`
`dsw` | `diff --staged --word-diff`
`f` | `fetch`
`fa` | `fetch --all`
`fap` | `fetch --all --prune`
`ll` | `log --oneline --max-count=50 --decorate --exclude=refs/stash`
`lg` | `log --oneline --max-count=30 --decorate --exclude=refs/stash --graph`
`s` | `status`

## Commands
| *description* | *command* | *link* |
| -------------:|:--------- |:------ |
create new repo | `git init` | [git-init](https://git-scm.com/docs/git-init)
clone repo | `git clone <path\|url> [<directory>]` | [git-clone](https://git-scm.com/docs/git-clone)
connect local repo to remote repo | `git remote add <name> <path\|url>` | [git-remote](https://git-scm.com/docs/git-remote)
 | | 
show commit changes | `git show [<commit>]` | [git-show](https://git-scm.com/docs/git-show)
 | |
add changes to INDEX | `git add [--patch] <files>` | [git-add](https://git-scm.com/docs/git-add)
reset changes from INDEX | `git reset HEAD <files>` | [git-reset](https://git-scm.com/docs/git-reset)
 | | 
create new branch | `git checkout -b <branch>` | [git-checkout](https://git-scm.com/docs/git-checkout)
switch to branch or commit | `git checkout <branch\|commit>` | [git-checkout](https://git-scm.com/docs/git-checkout)
delete branch | `git branch -d <branch>` | [git-branch](https://git-scm.com/docs/git-branch)
 | | 
add changes to stash | `git stash [push [--patch]] [-m <message>] <files>` | [git-stash](https://git-scm.com/docs/git-stash)
remove and apply stash | `git stash pop [--index] [-q\|--quiet] [<stash>]` | [git-stash](https://git-scm.com/docs/git-stash)
remove all stash entries | `git stash clear ` | [git-stash](https://git-scm.com/docs/git-stash)
 | | 
revert commit | `git revert [--no-edit] <commit>` | [git-revert](https://git-scm.com/docs/git-revert)
 | | 
commit changes | `git commit [-m <message>] ` | [git-commit](https://git-scm.com/docs/git-commit)
amend last commit | `git commit --amend [--no-edit]` | [git-commit](https://git-scm.com/docs/git-commit)
 | | 
copy commit | `git cherry-pick <commit>` | [git-cherry-pick](https://git-scm.com/docs/git-cherry-pick)
 | | 
sync local with remote branches | `git remote prune origin` | [git-remote](https://git-scm.com/docs/git-remote)
 | | 
ignore updates of tracked file | `git update-index --skip-worktree <file>` | [git-update-index](https://www.git-scm.com/docs/git-update-index)
 | |
add submodule | `git submodule add <path\|url> [<directory>]` | [git-submodule](https://git-scm.com/docs/git-submodule)
update submodule | `git submodule update [--init] [--recursive]` | [git-submodule](https://git-scm.com/docs/git-submodule)


## Workflows

### Semi-Linear History
[https://www.bitsnbites.eu/a-tidy-linear-git-history/](https://www.bitsnbites.eu/a-tidy-linear-git-history/)

| *step* | *description* | *command* |
| ------:|:-------------:| --------- |
1 | checkout *target* branch | `git checkout <branch>`
2 | pull on *target* branch | `git pull`
3 | checkout *feature* branch | `git checkout <branch>`
4 | rebase *feature* on *target* branch | `git rebase <branch>`
5 | checkout *target* branch | `git checkout <branch>`
6 | merge *feature* into *target* branch with **no-ff** | `git merge --no-ff <branch>`
7 | publish *target* branch | `git push origin <branch>`
