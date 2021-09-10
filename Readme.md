# Git is the free and open source distributed version control system that's responsible for everything GitHub related that happens locally on your computer. This cheat sheet features the most important and commonly used Git commands for easy reference.

## INSTALLATION & GUIS
With platform specific installers for Git, GitHub also provides the ease of staying up-to-date with the latest releases of the command line tool while providing a graphical user interface for day-to-day interaction, review, and repository synchronization.
### [GitHub for Windows](https://windows.github.com) 
### [GitHub for Mac](https://mac.github.com) 
### For Linux and Solaris platforms, the latest release is available on the official Git web site. 
### [Git for All Platforms](https://git-scm.com)

## SETUP

- Configuring user information used across all local repositories
- <code>git config --global user.name “[firstname lastname]”</code>
- set a name that is identifiable for credit when review version history
- <code>git config --global user.email “[valid-email]”</code>
- set an email address that will be associated with each history marker
- <code>git config --global color.ui auto</code>
- set automatic command line coloring for Git for easy reviewing

## SETUP & INIT

- Configuring user information, initializing and cloning repositories
- <code>git init</code>
- initialize an existing directory as a Git repository
- <code>git clone [url]</code>
- retrieve an entire repository from a hosted location via URL

## STAGE & SNAPSHOT

- Working with snapshots and the Git staging area
- <code>git status</code>
- show modified files in working directory, staged for your next commit
- <code>git add [file]</code>
- add a file as it looks now to your next commit (stage)
- <code>git reset [file]</code>
- unstage a file while retaining the changes in working directory
- <code>git diff</code>
- diff of what is changed but not staged
- <code>git diff --staged</code>
- diff of what is staged but not yet commited
- <code>git commit -m “[descriptive message]”</code>
- commit your staged content as a new commit snapshot

## BRANCH & MERGE
- Isolating work in branches, changing context, and integrating changes
- <code>git branch</code>
- list your branches. a * will appear next to the currently active branch
- <code>git branch [branch-name]</code>
- create a new branch at the current commit
- <code>git checkout</code>
- switch to another branch and check it out into your working directory
- <code>git merge [branch]</code>
- merge the specified branch’s history into the current one
- <code>git log</code>
- show all commits in the current branch’s history

## INSPECT & COMPARE

- Examining logs, diffs and object information
- <code>git log</code>
- show the commit history for the currently active branch
- <code>git log branchB..branchA</code>
- show the commits on branchA that are not on branchB
- <code>git log --follow [file]</code>
- show the commits that changed file, even across renames
- <code>git diff branchB...branchA</code>
- show the diff of what is in branchA that is not in branchB
- <code>git show [SHA]</code>
- show any object in Git in human-readable format

## TRACKING PATH CHANGES

- Versioning file removes and path changes
- <code>git rm [file]</code>
- delete the file from project and stage the removal for commit
- <code>git mv [existing-path] [new-path]</code>
- change an existing file path and stage the move
- <code>git log --stat -M</code>
- show all commit logs with indication of any paths that moved

## IGNORING PATTERNS

- Preventing unintentional staging or commiting of files
- <code>git config --global core.excludesfile [file]</code>
- system wide ignore patern for all local repositories
<code>logs/
*.notes
pattern*/</code>
- Save a file with desired paterns as .gitignore with either direct string matches or wildcard globs

## SHARE & UPDATE

- Retrieving updates from another repository and updating local repos
- <code>git remote add [alias] [url]</code>
- add a git URL as an alias
- <code>git fetch [alias]</code>
- fetch down all the branches from that Git remote
- <code>git merge [alias]/[branch]</code>
- merge a remote branch into your current branch to bring it up to date
- <code>git push [alias] [branch]</code>
- Transmit local branch commits to the remote repository branch
- <code>git pull</code>
- fetch and merge any commits from the tracking remote branch

## REWRITE HISTORY

- Rewriting branches, updating commits and clearing history
- <code>git rebase [branch]</code>
- apply any commits of current branch ahead of specified one
- <code>git reset --hard [commit]</code>
- clear staging area, rewrite working tree from specified commit

## TEMPORARY COMMITS

- Temporarily store modified, tracked files in order to change branches
- <code>git stash</code>
- Save modified and staged changes
- <code>git stash list</code>
- list stack-order of stashed file changes
- <code>git stash pop</code>
- write working from top of stash stack
- <code>git stash drop</code>
- discard the changes from top of stash stack
