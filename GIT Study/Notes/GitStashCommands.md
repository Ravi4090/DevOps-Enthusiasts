

## Git Stash

Git stash is a command in Git that allows you to save changes that are not ready to be committed yet, allowing you to switch branches or perform other operations without committing your changes. Below are some common Git stash commands:

1. **`git stash save "message"`** or **`git stash save`**
   - Saves the current changes in the working directory to a new stash with an optional message.

2. **`git stash list`**
   - Lists all stashes along with their reference names.

3. **`git stash apply`**
   - Applies the latest stash changes to the working directory. This leaves the stash in the list.

4. **`git stash apply stash@{n}`**
   - Applies a specific stash, identified by its index `n`.

5. **`git stash pop`**
   - Applies the latest stash changes and removes it from the stash list.

6. **`git stash pop stash@{n}`**
   - Applies a specific stash and removes it from the stash list.

7. **`git stash drop`**
   - Removes the latest stash without applying it.

8. **`git stash drop stash@{n}`**
   - Removes a specific stash without applying it.

9. **`git stash clear`**
   - Removes all stashes. Use with caution, as this action is irreversible.

10. **`git stash branch <branch_name>`**
    - Creates a new branch from the stash and switches to it.

11. **`git stash show`**
    - Displays the changes that are in the stash.

12. **`git stash show -p`** or **`git stash show --patch`**
    - Shows the changes in the stash as a diff.

