| S.No | Command                 | Syntax                            | Description                                       | Example                                            |
|------|-------------------------|-----------------------------------|---------------------------------------------------|----------------------------------------------------|
| 1    | `git init`              | `git init`                        | Initializes a new Git repository.                  | `git init`                                         |
| 2    | `git add`               | `git add <file>`                  | Adds changes from the working directory to the staging area. | `git add filename`                                 |
| 3    | `git commit`            | `git commit -m "Commit message"`  | Records changes from the staging area to the repository. | `git commit -m "Initial commit"`                   |
| 4    | `git status`            | `git status`                      | Shows the status of changes in the working directory. | `git status`                                       |
| 5    | `git log`               | `git log`                         | Displays the commit history.                      | `git log`                                          |
| 6    | `git diff`              | `git diff`                        | Shows changes between commits or the working directory. | `git diff`                                         |
| 7    | `git clone`             | `git clone <repository_url>`      | Copies a repository to create a local copy.       | `git clone https://github.com/example/repo.git`   |
| 8    | `git pull`              | `git pull origin master`          | Fetches and merges changes from a remote repository. | `git pull origin master`                           |
| 9    | `git push`              | `git push origin master`          | Uploads local changes to a remote repository.     | `git push origin master`                           |
| 10   | `git fetch`             | `git fetch origin`                | Retrieves changes from a remote repository without merging. | `git fetch origin`                                |
| 11   | `git merge`             | `git merge feature-branch`        | Combines changes from one branch into another.    | `git merge feature-branch`                         |
| 12   | `git branch`            | `git branch new-branch`           | Lists existing branches or creates a new branch. | `git branch new-feature`                           |
| 13   | `git checkout`          | `git checkout <branch>`           | Switches between branches or restores working tree files. | `git checkout feature-branch`                     |
| 14   | `git remote`            | `git remote -v`                   | Lists remote repositories associated with the current repository. | `git remote -v`                                    |
| 15   | `git pull request`      | `git pull-request`                | Submits a pull request in Git hosting platforms (GitHub, GitLab). | `git pull-request`                                |
| 16   | `git fetch --prune`     | `git fetch --prune`               | Fetches changes from remote and removes references to deleted branches. | `git fetch --prune`                               |
| 17   | `git reset`             | `git reset --hard HEAD^`          | Resets the current branch to a previous commit.   | `git reset --hard HEAD^`                           |
| 18   | `git revert`            | `git revert <commit_hash>`        | Creates a new commit that undoes changes from a previous commit. | `git revert abc123`                               |
| 19   | `git tag`               | `git tag -a v1.0 -m "Release v1.0"` | Creates an annotated tag for a specific commit.  | `git tag -a v1.0 -m "Release v1.0"`                 |
| 20   | `git stash`             | `git stash save "Work in progress"` | Temporarily saves changes that are not ready to be committed. | `git stash save "Work in progress"`               |
