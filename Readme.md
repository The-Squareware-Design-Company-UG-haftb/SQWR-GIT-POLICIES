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

## Branching
A branching strategy is a convention or a set of rules that specify when branches get created.
It helps teams and developers by describing the naming guidelines of branches and elaborates on what use the branches should have, and so on.
With a lack of appropriate naming conventions, the code maintenance team suffers numerous confusions and complications.
[Git](https://codingsight.com/git-branching-naming-convention-best-practices/?ref=hackernoon.com)  branching naming convention supports the organic growth of a codebase in a systematic way. It helps in separating the work strategically.
## The two broad categories of Git branches

**1. Regular Branches**
Available permanently in the repository, the naming convention of regular branches is easy and straightforward.

**Dev**
Dev, the main development branch, restricts developers from adding any changes in the master branch directly. Before merging to the master, changes made in the dev branch undergo reviews and tests.


**Master**


The Master branch is the default branch available in the Git repository. Team members need to keep the master branch stable and updated. It usually is stable and doesn't allow direct check-in. Merging is possible only after code review.


**QA or test branch**


This branch holds the QA codes and automation testing of the implemented changes. It ensures a stable codebase for the production environment through the QA testing process.


**2. Temporary Git branches**


Team members can create and delete these branches whenever it is required.

-   Own name Branch 
-   Bug Fix
-   Hot Fix
-   Feature Branches

There are a large number of recommended conventions and formats, following which could be a challenging task.



## The best practices of the Git branch naming convention

**1. Starting branch name with a category word**



One of the best methods to improve efficiency is by adding a word that categorizes the branch. The general idea is to use short words. The word selection could be anything that suits your working system.

Use category words such as:

1.  WIP - Work in progress and needs your attention.
2.  Bug - A bug or an error that needs fixing promptly.

With the help of the category word, it is effortless to identify the purpose of the  [Git branch](https://hackernoon.com/git-branches-vgaa3ypm?ref=hackernoon.com)  and attend to it.


**2. Using unique issue tracker IDs in branch names**


Prefixes such as; hotfix, feature, chore, or any other variant to categorize a task, increase the work requiring more decision-making while naming.


With unique issue tracker IDs, you are essentially marking the task's category in the tracker and adding many useful contexts.


Developers mostly work on several issues at a given time, and an issue tracker helps to connect the working branch with relevant tasks. It makes tracking team progress very easy.



Using an external issue tracking ID in the branch name can facilitate tracking the progress from external systems.


**3. Using hyphen or slash separators**


The preference between a hyphen, slash, or underscore separator is based on you and your team's choice. The idea is to keep it tightly consistent.



Without the separators, the names become more challenging to read, creating confusion for the team.


Using separators such as underscores, you can improve the readability and make the name more comfortable to manage.



Separators are especially more significant if you are dealing with a vast number of branches.


**4. Using author name in Git branch**


Numerous companies use this technique of adding the author's name to the branch names.


This method helps to track the work of different developers. With further requirements, progressive additions are also possible.

> Example - name_feature_new-experimental-changes

**5. Avoid using just numerals**


Using only numbers in the branch name's issue ID can lead to more confusion for the team.


Such confusion during the merging process of Git branches may lead to a lot of mistakes.


**6. Avoid simultaneous naming convention**


Blending or combining Git branch naming conventions only leads to complications and makes the process prone to errors. Consistency is a critical aspect, and the team should maintain the decided conventions.


**7. Avoid long names**



Precision is the crucial regard of Git branch naming. The name needs to be informative and short.


Long detailed names only lead to confusion and affect efficiency.



> Instead of, wip_login_module_which_will_used_in_the_public_website, you can opt for wip_feature_login_module.

The practices for Git branching naming are effective only upon the commitment of proper application. The critical element is that the team stays on the same page and remains consistent everywhere.


With the appropriate usage of the conventions, you and the team can remarkably improve work efficiency and flow.
