
# Module 4 : Important Git Commands

## 1. `init`

- **Usage**: `git init`
- **Purpose**: Initializes a new Git repository in the current directory.
- **Example**:
  ```bash
  $ mkdir my_project
  $ cd my_project
  $ git init
  ```
  This creates a new Git repository in the "my_project" directory.

## 2. `add`

- **Usage**: `git add <file>`
- **Purpose**: Adds changes in the working directory to the staging area.
- **Example**:
  ```bash
  $ git add file.txt
  ```
  Stages changes made to "file.txt" for the next commit.

## 3. `commit`

- **Usage**: `git commit -m "Commit message"`
- **Purpose**: Records the changes staged in the index to the repository.
- **Example**:
  ```bash
  $ git commit -m "Initial commit"
  ```
  Commits the staged changes with the commit message "Initial commit."

## 4. `status`

- **Usage**: `git status`
- **Purpose**: Shows the status of changes as untracked, modified, or staged.
- **Example**:
  ```bash
  $ git status
  ```
  Displays the current status of the working directory.

## 5. `log`

- **Usage**: `git log`
- **Purpose**: Displays a chronological log of commits.
- **Example**:
  ```bash
  $ git log
  ```
  Shows a detailed log including commit hashes, authors, dates, and commit messages.

## 6. `diff`

- **Usage**: `git diff`
- **Purpose**: Shows changes between commits, commit and working tree, etc.
- **Example**:
  ```bash
  $ git diff
  ```
  Displays the differences between the working directory and the last commit.

## 7. `clone`

- **Usage**: `git clone <repository_url>`
- **Purpose**: Creates a copy of a repository from a remote server.
- **Example**:
  ```bash
  $ git clone https://github.com/example/repo.git
  ```
  Creates a local copy of the remote repository.

## 8. `pull`

- **Usage**: `git pull <remote> <branch>`
- **Purpose**: Fetches changes from a remote repository and merges them into the current branch.
- **Example**:
  ```bash
  $ git pull origin master
  ```
  Fetches changes from the "master" branch on the remote repository.

## 9. `push`

- **Usage**: `git push <remote> <branch>`
- **Purpose**: Pushes local changes to a remote repository.
- **Example**:
  ```bash
  $ git push origin feature_branch
  ```
  Pushes local changes in the "feature_branch" to the remote repository.

## 10. `fetch`

- **Usage**: `git fetch <remote>`
- **Purpose**: Downloads objects and refs from a remote repository.
- **Example**:
  ```bash
  $ git fetch origin
  ```
  Fetches any new changes from the remote repository.

## 11. `merge`

- **Usage**: `git merge <branch>`
- **Purpose**: Combines changes from the specified branch into the current branch.
- **Example**:
  ```bash
  $ git merge feature_branch
  ```
  Merges changes from "feature_branch" into the current branch.

## 12. `branch`

- **Usage**: `git branch`, `git branch <branch_name>`
- **Purpose**: Lists existing branches or creates a new branch.
- **Example**:
  ```bash
  $ git branch
  ```
  Lists all branches in the repository.

## 13. `checkout`

- **Usage**: `git checkout <branch_or_commit>`
- **Purpose**: Switches branches or restores working tree files.
- **Example**:
  ```bash
  $ git checkout feature_branch
  ```
  Switches to the "feature_branch" in the repository.

These Git commands form the core set needed for version control and collaborative software development. Understanding and mastering these commands are crucial for efficient and effective use of Git.

