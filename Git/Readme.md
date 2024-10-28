# Git in DevOps
Git is an essential tool in DevOps for managing and tracking code changes. It enables collaboration, version control, and efficient code management, making it indispensable for DevOps engineers working in agile and CI/CD environments.

## Definition
Git is a distributed version control system that allows multiple developers to work on a project simultaneously. It tracks changes in source code during software development, facilitating collaboration and ensuring code integrity.

- **Developed by**: Linus Torvalds
- **Purpose**: Track changes in source code during software development

## 🧩 **Types of Git Repositories**

### 1. **Local Repository**
   - The repository on your local machine where you work on files and commit changes.
   - **Commands**:
     ```bash
     git init             # Initialize a new local repository
     git add .            # Stage files for commit
     git commit -m "Your message"   # Commit changes
     ```

### 2. **Remote Repository**
   - A shared repository hosted on platforms like GitHub, GitLab, or Bitbucket. 
   - Used to sync changes across different developers.
   - **Commands**:
     ```bash
     git remote add origin <repo_url>   # Link local repo to remote
     git push origin main                 # Push commits to remote main branch
     git pull origin main                 # Pull latest changes from remote main branch
     ```
---

## 🌐 **Public vs. Private Repositories**

| Type of Repo      | Description                                                                                     | Use Cases                                |
|-------------------|-------------------------------------------------------------------------------------------------|------------------------------------------|
| **Public Repo**   | Accessible to anyone; ideal for open-source projects where transparency and collaboration are key. | Open-source projects, public knowledge sharing |
| **Private Repo**  | Access is restricted; only selected users can view or contribute. Suitable for proprietary code. | Internal projects, sensitive codebases  |

### **How to Create a Public/Private Repository on GitHub:**
1. Go to **GitHub** and click on **New Repository**.
2. Name your repository and choose **Public** or **Private**.
3. Initialize with a **README** if needed, and click **Create Repository**.

---

## How and Why Git is Used
- **Collaboration**: Enables multiple developers to work on the same codebase without overwriting each other's changes.
- **Version Tracking**: Keeps a history of changes, allowing developers to revert to previous versions if necessary.
- **Branching and Merging**: Supports branching, enabling features to be developed in isolation and merged back into the main codebase.

## Basic Information
- **Commits**: Snapshots of changes made to files in a repository.
- **Branches**: Independent lines of development. The main branch is often called `main` or `master`.
- **Merges**: Combining changes from one branch into another.
- **Staging Area**: A place where changes are prepared before committing them to the repository.

## 🔄 **Why Use Git in DevOps?**

- **Version Control**: Maintains a history of changes, making it easy to revert if necessary.
- **Collaboration**: Allows multiple team members to work together on the same codebase.
- **Automation Integration**: Easily integrates with CI/CD tools like Jenkins, GitHub Actions, and GitLab CI for automated testing and deployments.

---

## Git Commands Explanation

| Explanation                                                                                                           | Commands                                 |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| Verify git installation                                                                                               | `git --version`                          |
| Sets up global configurations like username and email, affecting all repositories on the machine.                     | `git config --global user.name "Your Name"`<br>`git config --global user.email "you@example.com"` |
| Initializes a new Git repository in the current directory.                                                            | `git init`                               |
| Copies a remote repository to the local machine, creating a working copy.                                             | `git clone <repository_url>`             |
| Links a local repository to a remote, enabling push and pull operations.                                              | `git remote add origin <url>`            |
| Fetches and merges changes from a remote repository into the current branch.                                          | `git pull origin main`                   |
| Downloads changes from a remote repository without merging.                                                           | `git fetch origin`                       |
| Stages changes in the working directory, preparing them for commit.                                                   | `git add <file_name>` or `git add .`     |
| Records the staged changes as a new commit in the repository history.                                                 | `git commit -m "Commit message"`         |
| Uploads local commits to a remote repository branch.                                                                  | `git push origin main`                   |
| Lists, creates, or deletes branches, allowing parallel work in isolated code versions.                                | `git branch <branch_name>`               |
| Switches to another branch in the repository.                                                                         | `git switch <branch_name>`               |
| Switches branches or restores files to a specific commit or branch.                                                   | `git checkout <branch_name>`             |
| Shows a history of commits with messages, authors, and timestamps.                                                    | `git log`                                |
| Displays the current state of the working directory and staging area.                                                 | `git status`                             |
| Temporarily saves changes not ready for commit and clears the working directory.                                      | `git stash`                              |
| Restores the most recent stash and removes it from the stash list.                                                    | `git stash pop`                          |
| Creates a tag to mark a specific commit, often used for version releases.                                             | `git tag v1.0`                           |
| Merges changes from another branch into the current branch.                                                           | `git merge <branch_name>`                |
| Re-applies commits on top of another branch, creating a linear history.                                               | `git rebase <branch_name>`               |
| Resets the current HEAD to a specific commit, useful for undoing commits.                                             | `git reset <commit_id>`                  |
| Shows differences between working directory changes and the last commit.                                              | `git diff`                               |
| Removes a file from the working directory and stages its deletion.                                                    | `git rm <file_name>`                     |
| Applies a specific commit from another branch onto the current branch.                                                | `git cherry-pick <commit_id>`            |
| Shows a log of all changes made to HEAD, helpful for recovering lost commits.                                         | `git reflog`                             |
| Displays details of a specific commit.                                                                                | `git show <commit_id>`                   |
| Cancels an in-progress merge, reverting back to the pre-merge state.                                                  | `git merge --abort`                      |
| Cancels an in-progress rebase, reverting to the pre-rebase state.                                                     | `git rebase --abort`                     |
| Continues a rebase after resolving conflicts.                                                                         | `git rebase --continue`                  |
| Interactively rebases to edit, re-order, or squash commits.                                                           | `git rebase -i HEAD~3`                   |
| Sets configurations on a repository level, including user name and email.                                             | `git config user.name "Your Name"`<br>`git config user.email "you@example.com"` |
| Creates a compressed archive file of a commit or branch.                                                              | `git archive --format=zip HEAD > archive.zip` |
| Shows who modified each line in a file.                                                                               | `git blame <file_name>`                  |
| Removes untracked files from the working directory.                                                                   | `git clean -f`                           |
| Uses binary search to find the commit that introduced a bug.                                                          | `git bisect start`                       |
| Creates a new commit that undoes changes made by a previous commit.                                                   | `git revert <commit_id>`                 |
| Edits the most recent commit, changing the commit message or adding more changes.                                     | `git commit --amend`                     |
| Sets an alias for a commonly used command to simplify Git workflows.                                                  | `git config --global alias.st status`    |
| Moves HEAD to a previous commit while keeping staged changes.                                                         | `git reset --soft <commit_id>`           |
| Moves HEAD to a previous commit and discards all changes after it.                                                    | `git reset --hard <commit_id>`           |
| Lists all stashes, showing a summary of saved states.                                                                 | `git stash list`                         |
| Applies a saved stash without deleting it from the stash list.                                                        | `git stash apply stash@{0}`              |
| Groups commit messages by author, useful for summaries.                                                               | `git shortlog -sn`                       |
| Manages sub-projects in a main project, useful for large monorepos.                                                   | `git subtree add --prefix=<path> <repo> <branch>` |
| Runs garbage collection to optimize the local repository.                                                             | `git gc`                                 |
| Adds an additional working tree to an existing repository, allowing multiple branches in separate folders.            | `git worktree add <path> <branch>`       |
| Configures Git to use a merge (instead of a rebase) when pulling changes from a remote branch.                        | `git config pull.rebase false`           |
| Sets the upstream branch for the current local branch, making future git push and git pull commands easier.           | `git push --set-upstream origin main`    |
| Unstages a file that has been added to staging area, moving it back to working directory(reverts a git add action).   | `git restore --staged <file_name>`       |
| Renames the current branch to "main." Commonly used to rename "master" to "main" as the primary branch name.          | `git branch -M main`                     |

