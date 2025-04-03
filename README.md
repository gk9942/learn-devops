# learn-devops
used for devops learnings

Commands
Git add
Moves changes from the working directory to the staging area. This gives you the opportunity to prepare a snapshot before committing it to the official history.

Related tutorials
Saving changes: git add
Learn Git with Bitbucket Cloud: Copy your Git repository and add files
Using branches: git merge
Inspecting a repository: git status
Git branch
This command is your general-purpose branch administration tool. It lets you create isolated development environments within a single repository.

Related tutorials
Using branches: git branch
Using branches: git checkout
Using branches: git merge
Learn Git with Bitbucket Cloud: Use a Git branch to merge a file
Git checkout
In addition to checking out old commits and old file revisions, git checkout is also the means to navigate existing branches. Combined with the basic Git commands, it’s a way to work on a particular line of development.

Related tutorials
Using branches: git checkout
Undoing changes: git checkout
Comparing workflows: Gitflow workflow
Git clean
Removes untracked files from the working directory. This is the logical counterpart to git reset, which (typically) only operates on tracked files.

Related tutorials
Undoing changes: git clean
Git clone
Creates a copy of an existing Git repository. Cloning is the most common way for developers to obtain a working copy of a central repository.

Related tutorials
Git LFS
Comparing workflows: Forking workflow
Setting up a repository: git clone
Git commit
Takes the staged snapshot and commits it to the project history. Combined with git add, this defines the basic workflow for all Git users.

Related tutorials
Using branches: git merge
Rewriting history: git commit --amend
Learn Git with Bitbucket Cloud: Copy your Git repository and add files
Saving changes: git add
git commit --amend
Passing the --amend flag to git commit lets you amend the most recent commit. This is very useful when you forget to stage a file or omit important information from the commit message.

Related tutorials
Rewriting history: git commit --amend
git config
A convenient way to set configuration options for your Git installation. You’ll typically only need to use this immediately after installing Git on a new development machine.

Related tutorials
Setting up a repository: git config
Git LFS
Install Git: Install Git on Mac OS X
Install Git: Install Git on Linux
git fetch
Fetching downloads a branch from another repository, along with all of its associated commits and files. But, it doesn't try to integrate anything into your local repository. This gives you a chance to inspect changes before merging them with your project.

Related tutorials
Syncing: git fetch
Refs and the reflog: Refspecs
Syncing: git pull
git init
Initializes a new Git repository. If you want to place a project under revision control, this is the first command you need to learn.

Related tutorials
Setting up a repository: git init
git log
Lets you explore the previous revisions of a project. It provides several formatting options for displaying committed snapshots.

Related tutorials
Inspecting a repository: git log
Advanced Git log: Filtering the commit history
Advanced Git log: Formatting log output
Advanced Git tutorials: Overview
git merge
A powerful way to integrate changes from divergent branches. After forking the project history with git branch, git merge lets you put it back together again.

Related tutorials
Merging vs. rebasing: Workflow walkthrough
Using branches: git merge
Comparing workflows: Gitflow workflow
Merging vs. rebasing: Conceptual overview
git pull
Pulling is the automated version of git fetch. It downloads a branch from a remote repository, then immediately merges it into the current branch. This is the Git equivalent of svn update.

Related tutorials
Syncing: git pull
Comparing workflows: Centralized workflow
Git LFS
Comparing workflows: Forking workflow
git push
Pushing is the opposite of fetching (with a few caveats). It lets you move a local branch to another repository, which serves as a convenient way to publish contributions. This is like svn commit, but it sends a series of commits instead of a single changeset.

Related tutorials
Syncing: git push
Refs and the reflog: Refspecs
Comparing workflows: Gitflow workflow
Git LFS
git rebase
Rebasing lets you move branches around, which helps you avoid unnecessary merge commits. The resulting linear history is often much easier to understand and explore.

Related tutorials
Merging vs. rebasing: Workflow walkthrough
Rewriting history: git rebase -i
Merging vs. rebasing: Conceptual overview
Rewriting history: git rebase
git rebase -i
The -i flag is used to begin an interactive rebasing session. This provides all the benefits of a normal rebase, but gives you the opportunity to add, edit, or delete commits along the way.

Related tutorials
Rewriting history: git rebase -i
git reflog
Git keeps track of updates to the tip of branches using a mechanism called reflog. This allows you to go back to changesets even though they are not referenced by any branch or tag.

Related tutorials
Rewriting history: git reflog
git remote
A convenient tool for administering remote connections. Instead of passing the full URL to the fetch, pull, and push commands, it lets you use a more meaningful shortcut.

Related tutorials
Syncing: git remote
git reset
Undoes changes to files in the working directory. Resetting lets you clean up or completely remove changes that have not been pushed to a public repository.

Related tutorials
Undoing changes: git reset
Reset, checkout, and revert: Commit-level operation
Reset, checkout, and revert: File-level operation
Undoing changes: git clean
git revert
Undoes a committed snapshot. When you discover a faulty commit, reverting is a safe and easy way to completely remove it from the code base.

Related tutorials
Undoing changes: git revert
Reset, checkout, and revert: Commit-level operation
Reset, checkout, and revert: Summary
git status
Displays the state of the working directory and the staged snapshot. You’ll want to run this in conjunction with git add and git commit to see exactly what’s being included in the next snapshot.

Related tutorials
Inspecting a repository: git status
Git stash
Learn Git with Bitbucket Cloud: Use a Git branch to merge a file
Learn Git with Bitbucket Cloud: Copy your Git repository and add files
Terminology
Branch
A branch represents an independent line of development. Branches serve as an abstraction for the edit/stage/commit process discussed in Git Basics, the first module of this series. You can think of them as a way to request a brand new working directory, staging area, and project history. New commits are recorded in the history for the current branch, which results in a fork in the history of the project.

Related tutorials
Learn Git with Bitbucket Cloud: Use a Git branch to merge a file
Comparing workflows: Gitflow workflow
Using branches: git branch
Comparing workflows: Feature branch workflow
Centralized workflow
If your developers are already comfortable with Subversion, the Centralized Workflow lets you experience the benefits of Git without having to adapt to an entirely new process. It also serves as a friendly transition into more Git-oriented workflows.

Related tutorials
Comparing workflows: Feature branch workflow
Feature branch workflow
The Feature Branch Workflow builds on the Centralized Workflow by encapsulating new features into dedicated branches. This enables the use of pull requests as a means to discuss changes before they’re integrated into the official project.

Related tutorials
Comparing workflows: Gitflow workflow
Making a pull request: How it works
Comparing workflows: Feature branch workflow
Why Git for your organization: Git for developers
Forking
Instead of using a single server-side repository to act as the “central” codebase, forking gives every developer a server-side repository. This means that each contributor has not one, but two Git repositories: a private local one and a public server-side one.

Related tutorials
Comparing workflows: Forking workflow
Making a pull request: How it works
Gitflow workflow
The Gitflow Workflow streamlines the release cycle by using isolated branches for feature development, release preparation, and maintenance. Its strict branching model also lends some much needed structure to larger projects.

Related tutorials
Making a pull request: How it works
Comparing workflows: Gitflow workflow
HEAD
Git’s way of referring to the current snapshot. Internally, the git checkout command simply updates the HEAD to point to either the specified branch or commit. When it points to a branch, Git doesn't complain, but when you check out a commit, it switches into a “detached HEAD” state.

Related tutorials
Refs and the reflog: Special refs
Git hooks: Local hooks
Refs and the reflog: The reflog
Reset, checkout, and revert: Commit-level operation
Hook
A script that runs automatically every time a particular event occurs in a Git repository. Hooks let you customize Git’s internal behavior and trigger customizable actions at key points in the development life cycle.

Related tutorials
Git hooks: Conceptual overview
Git hooks: Local hooks
Git hooks: Server-side hooks
Git hooks
Main
The default development branch. Whenever you create a git repository, a branch named "main" is created, and becomes the active branch.

Related tutorials
Comparing workflows: Gitflow workflow
Comparing workflows: Feature branch workflow
Git stash
Learn Git with Bitbucket Cloud: Use a Git branch to merge a file
Pull request
Pull requests are a feature that makes it easier for developers to collaborate using Bitbucket. They provide a user-friendly web interface for discussing proposed changes before integrating them into the official project.

Related tutorials
Making a pull request: How it works
Making a pull request: Example
Comparing workflows: Feature branch workflow
Learn about code review in Bitbucket Cloud: Create a pull request
Repository
A collection of commits, and branches and tags to identify commits.

Related tutorials
Comparing workflows: Forking workflow
Learn Git with Bitbucket Cloud: Create a Git repository
Git LFS
Tag
A reference typically used to mark a particular point in the commit chain. In contrast to a head, a tag is not updated by the commit command.

Related tutorials
Convert
Undoing changes: git reset
Git stash
Saving changes: git add
Version control
A system that records changes to a file or set of files over time so that you can recall specific versions later.
