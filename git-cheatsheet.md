# Git Cheat Sheet
> Cheat sheet by Github.

## Configure tooling

`$ git config --global user.name "[name]"`
Sets the name you want attached to your commit transactions.

`$ git config --global user.email "[email address]"`
Sets the email you want attached to your commit transactions.

`$ git config --global color.ui auto`
Enables helpful colorization of command line output.

## Create repositories

`$ git init`
Turn current directory into a git repository.

`$ git remote add origin [url]`
Specifies the remote repository for your local repository.

`$ git clone [url]`
Clone a repository that already exists including all files, branches and commits.

## Branches
Any commits you make will be made on the branch you're currently "checked out" to.
Use `git status` to see which branch that is.

`$ git branch [branch-name]`
Creates a new branch.

`$ git switch -c [branch-name]`
or
`$ git checkout [branch-name]`
Switches to the specified branch and updates the working directory.

`$ git merge [branch]`
Combines the specified branch's history into the current branch.
This is usually done in PR (Pull Requests), but is an important git operation.

`$ git branch -d [branch-name]`
Deletes the specified branch.

## Synchronize changes
Synchronize local repository with the remote repository.

`$ git fetch`
Downloads all history from the remote tracking branches.

`$ git merge`
Combines remote tracking branch into current local branch.

`$ git push`
Uploads all local branch commits to remote repository.

`$ git pull`
Updates your current local working branch with all new commits from the corresponding remote branch.

## Make changes
Browse and inspect the evolution of project files.

`$ git log`
Lists version history for the current branch.

`$ git log --follow [file]`
Lists version history for a file, including renames.

`$ git diff [first-branch]...[second-branch]`
Shows content differences between two branches.

`$ git show [commit]`
Outputs metadata and content changes of the specified commit.

`$ git add [file]`
Snapshots the file in preparation for versioning.

`$ git commit -m "[descriptive message]"`
Records file snapshots permanently in version history.

## Redo commits
Erase mistakes and craft replacement history.

`$ git reset [commit]`
Undoes all commits after [commit], preserving changes locally.

`$ git reset --hard [commit]`
Discards all history and changes back to the specified commit.

## Github flow
```
                                        'master' branch
--()--------------------------------------------------------------------------------------()---
   \ Create 'feature' branch from 'master'            Merge 'feature' branch into 'master' /
    \                                                                                     /
     \----------()-------()-------()-------()-------()-------()-------()----------/
                   Commit changes          Submit PR        Review and commit
```


## Glossary

* **git**:        an open source, distributed version-control system.
* **GitHub**:     a platform for hosting and collaborating on Git repositories.
* **commit**:     a Git object, a snapshot of your entire repository compressed into a SHA.
* **branch**:     a lightweight movable pointer to a commit.
* **clone**:      a local version of a repository, including all commits and branches.
* **remote**:     a common repository on GitHub that all team member use to exchange their changes.
* **fork**:       a copy of a remote repository owned by a different user.
* **pull**        request: a place to compare and discuss the differences introduced on a branch with reviews, comments, integrated tests, and more.
* **HEAD**:       representing your current working directory, the HEAD pointer can be moved to different branches, tags, or commits when using git checkout.
