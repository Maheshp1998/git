# git
***************************************************************************************************************
**Configuration**
git config: Set user name and email globally.
>>>>>>>>>>>>>
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"
----------------------------------------------------------------------------------------------------------------

**Starting a Repository**
git init: Initialize a new Git repository.
>>>>>>>>>>>>>
git init
----------------------------------------------------------------------------------------------------------------

git clone: Clone an existing repository.
>>>>>>>>>>>>>
git clone https://github.com/example/repository.git
----------------------------------------------------------------------------------------------------------------

**Basic Snapshotting**
git add: Stage changes for commit.
>>>>>>>>>>>>>
git add filename.txt       # Stage a specific file
git add .                  # Stage all changes

git status: Check the status of your working directory.
>>>>>>>>>>>>>
git status
git diff: Show differences not yet staged.
>>>>>>>>>>>>>
git diff
----------------------------------------------------------------------------------------------------------------

**Committing Changes**
git commit: Commit staged changes with a message.
>>>>>>>>>>>>>
git commit -m "Commit message"
----------------------------------------------------------------------------------------------------------------

**Branching and Merging**
git branch: List, create, or delete branches.
>>>>>>>>>>>>>
git branch                      # List all branches
git branch new-branch           # Create a new branch
git branch -d branch-name       # Delete a branch
----------------------------------------------------------------------------------------------------------------

**git checkout: Switch to a different branch.**
>>>>>>>>>>>>>
git checkout branch-name        # Switch to an existing branch
git checkout -b new-branch      # Create and switch to a new branch

----------------------------------------------------------------------------------------------------------------

git merge: Merge changes from one branch to another.
>>>>>>>>>>>>>
git merge branch-name           # Merge branch into current branch
----------------------------------------------------------------------------------------------------------------

**Inspecting and Comparing**
git log: View commit history.
>>>>>>>>>>>>>
git log
----------------------------------------------------------------------------------------------------------------

git show: Show information about a specific commit.
>>>>>>>>>>>>>
git show commit-hash
----------------------------------------------------------------------------------------------------------------

**Sharing and Updating**
git push: Push commits to a remote repository.
>>>>>>>>>>>>>
git push origin branch-name     # Push commits to a specific branch
-----------------------------------------------------

git pull: Fetch and merge changes from a remote repository.
>>>>>>>>>>>>>
git pull origin branch-name     # Pull changes from a specific branch
-----------------------------------------------------

git fetch: Download objects and refs from a remote repository.
>>>>>>>>>>>>>
git fetch origin                # Fetch changes from the remote
-----------------------------------------------------

**Undoing Changes**
git revert: Undo a commit by creating a new commit.
>>>>>>>>>>>>>
git revert commit-hash          # Revert a specific commit
-----------------------------------------------------

git reset: Reset current HEAD to the specified state.
>>>>>>>>>>>>>
git reset --hard HEAD~1        # Reset to the previous commit
-----------------------------------------------------

**Stashing Changes**
git stash: Stash changes in the working directory.
>>>>>>>>>>>>>
git stash                      # Stash changes
git stash apply                # Apply stashed changes
----------------------------------------------------------------------------------------------------------------

**Miscellaneous**
git remote: Manage connections to remote repositories.
>>>>>>>>>>>>>
git remote -v                  # List remote repositories
----------------------------------------------------------------------------------------------------------------

git tag: Create, list, delete, or verify tags.
>>>>>>>>>>>>>
git tag                        # List tags
git tag -a v1.0 -m "Tag message"   # Create an annotated tag
git tag -d tag-name            # Delete a tag
----------------------------------------------------------------------------------------------------------------

git clean: Remove untracked files from the working tree.
>>>>>>>>>>>>>
git clean -n                   # Dry run (show what would be deleted)
git clean -f                   # Force delete untracked files
----------------------------------------------------------------------------------------------------------------

**These examples cover various scenarios and commands used in Git for version control and collaboration. Adjust these commands with your specific repository and workflow needs.**








delete branchs
origin---------
git push origin --delete branch_name

local -------
git branch -d staging
To force delete (even if not fully merged):
git branch -D staging


merge branchs ***************
git checkout staging
git pull origin staging
git checkout your_branch
git merge origin?staging
git push origin your_branch


-----to see the brnchs ***********
origin-----
git ls-remote --heads origin

local-------
git branch -r


Configure tooling
Configure user information for all local repositories
$ git config --global user.name "[name]"

Create repositories**************
Sets the name you want attached to your commit transactions
$ git init
Turn an existing directory into a git repository
$ git clone [url]
Clone (download) a repository that already exists on
GitHub, including all of the files, branches, and commits
The .gitignore file
Sometimes it may be a good idea to exclude files from being
tracked with Git. This is typically done in a special file named
.gitignore . You can find helpful templates for .gitignore
