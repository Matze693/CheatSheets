# git
| *description* | *command* | *link* |
| -------------:|:--------- | ------ |
create new repo | `git init` | | [git-init](https://git-scm.com/docs/git-init)
clone repo | `git clone <path\|url> [<directory>]` | [git-clone](https://git-scm.com/docs/git-clone)
connect local repo to remote repo | `git remote add <name> <path\|url>` | [git-remote](https://git-scm.com/docs/git-remote)
 | | 
add changes to INDEX | `git add [--patch] <files>` | [git-add](https://git-scm.com/docs/git-add)
reset changes from INDEX | `git reset HEAD <files>` | [git-reset](https://git-scm.com/docs/git-reset)
 | | 
create new branch | `git checkout -b <branch>` | [git-checkout](https://git-scm.com/docs/git-checkout)
switch to branch or commit | `git checkout <branch\|commit>` | [git-checkout](https://git-scm.com/docs/git-checkout)
delete branch | `git branch -d <branch>` | [git-branch](https://git-scm.com/docs/git-branch)
 | | 
add changes to stash | `git stash [push [--patch]] [-m <message>] <files>` | [git-stash](https://git-scm.com/docs/git-stash)
remove all stash entries | `git stash clear ` | [git-stash](https://git-scm.com/docs/git-stash)
 | | 
 revert commit | `git revert [--no-edit] <commit>` | [git-revert](https://git-scm.com/docs/git-revert)
 | | 
 commit changes | `git commit [-m <message>] ` | [git-commit](https://git-scm.com/docs/git-commit)
 amend last commit | `git commit --amend [--no-edit]` | [git-commit](https://git-scm.com/docs/git-commit)
