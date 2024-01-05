# 1. Sudo

## What is sudo?

**sudo** stands for "superuser do." It's a command used in Unix and Unix-like operating systems, including Linux, to allow a permitted user to execute a command as the superuser (or another user), as specified in the security policy.

## Key Points:

### Superuser Privileges:

- The superuser, often referred to as "root," has unrestricted access to all commands and files on a Linux system.
- `sudo` allows a regular user to perform administrative tasks with superuser privileges for specific commands.

### Usage:

- A user can execute a command with `sudo` by prefixing the command with it.
  - Example: `sudo apt update` allows a user to update the package list, a task that typically requires superuser privileges.

### Security:

- `sudo` is designed to enhance security by allowing specific users to execute only authorized commands as superuser.
- Users need to be explicitly listed in the sudoers file and enter their own password to use `sudo`.

### Configuration:

- Configuration settings for `sudo` are typically found in the `/etc/sudoers` file.
- The file allows specifying which users or groups are permitted to use `sudo` and the commands they can run.

# 2. Su

## What is su?

**su** stands for "switch user." It's a command that allows a user to become another user, typically the superuser (root), after entering the target user's password.

## Key Points:

### Switching Users:

- `su` allows a user to log in as another user, and by default, it switches to the superuser account.
  - Example: `su` prompts for the superuser's password and, if correct, grants access to the superuser account.

### Complete User Switch:

- When you use `su` without specifying a username, it switches to the superuser account.
  - Example: `su` (enters superuser mode).

### Temporary Superuser Access:

- Unlike `sudo`, which is often used to execute specific commands with superuser privileges, `su` grants the user access to the entire superuser environment.

### Root Password:

- To use `su` to become the superuser, you need to enter the root password.
  - Example: `su` prompts for the root password.

## Comparison: `sudo` vs. `su`

- `sudo` provides a more fine-grained approach, allowing specific users to execute authorized commands.
- `su` provides complete access to the target user's environment, often used to switch to the superuser.

## Use Cases:

- `sudo` is commonly used for specific administrative tasks.
- `su` is used when complete superuser access is needed.
