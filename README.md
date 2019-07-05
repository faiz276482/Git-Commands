
___
 
_A list of my commonly used Git commands_
 
--
 
### Getting & Creating Projects
 
| Command | Description |
| ------- | ----------- |
| `git init` | Initialize a local Git repository |
| `git clone ssh://git@github.com/[username]/[repository-name].git` | Create a local copy of a remote repository |
 
### Basic Snapshotting
 
| Command | Description |
| ------- | ----------- |
| `git status` | Check status |
| `git mv [source] [destination]` | It moves a file (or folder) to another folder or directory |
| `git mv -v [source] [destination] ` | (-v or --verbose) Report the names of files as they are moved. |
| `git mv -n [source] [destination] ` | (-n or --dry-run)Do nothing; only show what would happen |
| `git mv -f [source] [destination] ` | (-f or --force)Force renaming or moving of a file even if the target exists |
| `git mv -k [source] [destination] ` | (-k) Skip move or rename actions which would lead to an error condition. An error happens when a source is neither existing nor controlled by Git, or when it would overwrite an existing file unless [-f] is given. |
| `git add [file]` | Add a file to the staging area |
| `git add -A` | Add all new and changed files to the staging area |
| `git commit -m "[commit message]"` | Commit changes |
| `git rm -r [file]` | Remove a file (or folder) |
| `git reset` | Reset removes all the file currently present in staging area |
| `git reset --hard` | Resets the index and working tree. Any changes to tracked files in the working tree since <commit> are discarded. |
| `git reset --soft` | Does not touch the index file or the working tree at all (but resets the head to <commit>, just like all modes do). This leaves all your changed files "Changes to be committed", as git status would put it. |
| `git reset --mixed` | Resets the index but not the working tree (i.e., the changed files are preserved but not marked for commit) and reports what has not been updated. This is the default action.If -N is specified, removed paths are marked as intent-to-add |
| `git reset --keep` | Resets index entries and updates files in the working tree that are different between <commit> and HEAD. If a file that is different between <commit> and HEAD has local changes, reset is aborted. |
| `git reset --merge` | Resets the index and updates the files in the working tree that are different between <commit> and HEAD, but keeps those which are different between the index and working tree (i.e. which have changes which have not been added). If a file that is different between <commit> and the index has unstaged changes, reset is aborted.In other words, --merge does something like a git read-tree -u -m <commit>, but carries forward unmerged index entries. |
| `git reset [-q / --quiet  /--no-quiet] [<tree-ish>] [--] <paths>…` | Be quiet, only report errors. The default behavior is set by the reset.quiet config option. --quiet and --no-quiet will override the default behavior. |
 
### Branching & Merging
 
| Command | Description |
| ------- | ----------- |
| `git branch` | List branches (the asterisk denotes the current branch) |
| `git branch -a` | List all branches (local and remote) |
| `git branch [branch name]` | Create a new branch |
| `git branch -d [branch name]` | Delete a branch |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git checkout -b [branch name]` | Create a new branch and switch to it |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it |
| `git checkout [branch name]` | Switch to a branch |
| `git checkout -` | Switch to the branch last checked out |
| `git checkout -- [file]` | Discard changes to a file |
| `git merge [branch name]` | Merge a branch into the active branch |
| `git merge [source branch] [target branch]` | Merge a branch into a target branch |
| `git stash` | Stash changes in a dirty working directory |
| `git stash clear` | Remove all stashed entries |
 
### Sharing & Updating Projects
 
| Command | Description |
| ------- | ----------- |
| `git push origin [branch name]` | Push a branch to your remote repository |
| `git push -u origin [branch name]` | Push changes to remote repository (and remember the branch) |
| `git push` | Push changes to remote repository (remembered branch) |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git pull` | Update local repository to the newest commit |
| `git pull origin [branch name]` | Pull changes from remote repository |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git` | Add a remote repository |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Set a repository's origin branch to SSH |
| `git remote add upstream https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git` | Set a upstream repostory to compare your cahnges with the original owners master branch which you have forked |
 
### Inspection & Comparison
 
| Command | Description |
| ------- | ----------- |
| `git log` | View changes |
| `git log --summary` | View changes (detailed) |
| `git log -u` | View changes (detailed) |
| `git log -n <number a>` | view just one change that happened at ath commit from last commit |
| `git diff [source branch] [target branch]` | Preview changes before merging |
| `git diff [commitID1] [commitID2]` | Preview changes b/w two commits |
| `git diff --staged` | Preview changes b/w edited file and the file before editing at the staging area |

### Patching

| Command | Description |
| ------- | ----------- |
| `git rebase` | Reapply commits on top of another base tip |
| `git rebase --onto <newbase>` | Starting point at which to create the new commits. If the --onto option is not specified, the starting point is <upstream>. May be any valid commit, and not just an existing branch name.As a special case, you may use "A...B" as a shortcut for the merge base of A and B if there is exactly one merge base. You can leave out at most one of A and B, in which case it defaults to HEAD. |
| `git rebase <upstream>` | Upstream branch to compare against. May be any valid commit, not just an existing branch name. Defaults to the configured upstream for the current branch |
| `git rebase <branch_name>` | Working branch; defaults to HEAD. |
| `git rebase --continue` | Restart the rebasing process after having resolved a merge conflict. |
| `git rebase --abort` | Abort the rebase operation and reset HEAD to the original branch. If <branch> was provided when the rebase operation was started, then HEAD will be reset to <branch>. Otherwise HEAD will be reset to where it was when the rebase operation was started. |
| `git rebase --quit` | Abort the rebase operation but HEAD is not reset back to the original branch. The index and working tree are also left unchanged as a result. |
| `git rebase --keep-empty` | Keep the commits that do not change anything from its parents in the result |
| `git rebase --skip` | Restart the rebasing process by skipping the current patch. |

*If you are interested in learning more commands, have a look at https://git-scm.com/docs*
