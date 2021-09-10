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
