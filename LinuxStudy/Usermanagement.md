# User Management in Linux

Managing users and groups in a Linux environment is an essential administrative task that involves creating, modifying, and deleting user accounts. Here are some key commands and concepts related to user management:

## Commands:
- **useradd**: Adds a new user to the system.
- **userdel**: Deletes a user account.
- **groupadd**: Adds a new group.
- **groupdel**: Deletes a group.
- **usermod**: Modifies user account properties.

## System Files:
- **/etc/passwd**: Contains user account information.
- **/etc/group**: Holds group information.
- **/etc/shadow**: Stores encrypted password information.

## Root Access:
Performing administrative tasks requires root access. Use `sudo` before each command if you are a regular user, or log in as a sudo user.

-----

## Creating Users - First Approach:

1. **useradd:**
   - Use: `sudo useradd username`
   - Verification: `id username`

-----

## Creating Users - Second Approach: Recomended 

1. **useradd with Options:**
   - Command: `sudo useradd -g <groupname> -s /bin/bash -c "Comment" -m -d /home/username username`
   - Explanation of Options:
     - `-g <groupname>`: Sets the initial login group.
     - `-s /bin/bash`: Defines the default shell.
     - `-c "Comment"`: Adds a user comment or description.
     - `-m`: Creates the user's home directory.
     - `-d /home/username`: Specifies the home directory.

   - Example: 
     ```bash
     sudo useradd -g mygroup -s /bin/bash -c "John Doe - Software Engineer" -m -d /home/johndoe johndoe
     ```
     - The user is part of the group `mygroup`.
     - Default shell: `/bin/bash`.
     - Comment: "John Doe - Software Engineer."
     - Home directory: `/home/johndoe`.
     - Username: `johndoe`.

-----

## Deleting Users:

1. **userdel:**
   - Command: `sudo userdel username`
   - Example: `sudo userdel johndoe`
   - Removes the user account but retains the home directory and mail spool.

2. **userdel -r:**
   - Command: `sudo userdel -r username`
   - Example: `sudo userdel -r johndoe`
   - Deletes the user account along with the home directory and mail spool.

   - **Note:**
     - Keeping the home directory may be desirable for reasons such as backup, data recovery, recreation of user accounts, shared resources, and mail spool preservation.

----




-----
# Modifying User Attributes with `usermod` Command

To modify a user's attributes such as the initial login group, default shell, user comment, home directory, you can use the `usermod` command. Here's how you can do it with practical examples:

### 1. Modify Initial Login Group (`-g` option):

```bash
sudo usermod -g newgroup username
```

Replace "newgroup" with the desired group name, and "username" with the username of the user you want to modify.

### 2. Modify Default Shell (`-s` option):

```bash
sudo usermod -s /bin/zsh username
```

Replace "/bin/zsh" with the desired shell, and "username" with the username of the user you want to modify.

### 3. Add User Comment (`-c` option):

```bash
sudo usermod -c "New Comment" username
```

Replace "New Comment" with the new user comment, and "username" with the username of the user you want to modify.

### 4. Modify Home Directory (`-m` option not needed here):

```bash
sudo usermod -d /new/home/directory username
```

Replace "/new/home/directory" with the new home directory path, and "username" with the username of the user you want to modify.

### Practical Example:

Let's say you want to modify the user "john" with the following changes:
- Change the initial login group to "staff."
- Change the default shell to "/bin/zsh."
- Add a new comment for the user.
- Modify the home directory to "/home/john_new."

```bash
sudo usermod -g staff -s /bin/zsh -c "John Doe - Updated" -d /home/john_new john
```

This command makes the specified modifications for the user "john."

Always ensure that you have the necessary administrative privileges to modify user accounts, and double-check your changes to avoid unintended consequences.



----

# Locking and Unlocking User Accounts with `usermod` Command

Let's discuss in detail the `-L` and `-U` options with the `usermod` command, which are used to lock and unlock a user account, respectively.

## 1. Locking a User Account (`-L` option):

The `-L` option is used to lock a user account. When an account is locked, the user is prevented from logging in. It does not affect the user's password or any other account information. Locking an account is useful in situations where you want to temporarily prevent a user from accessing the system.

### Syntax:

```bash
sudo usermod -L username
```

### Example:

```bash
sudo usermod -L john
```

This command locks the user account named "john."

## 2. Unlocking a User Account (`-U` option):

The `-U` option is used to unlock a previously locked user account. When you unlock an account, the user is once again allowed to log in.

### Syntax:

```bash
sudo usermod -U username
```

### Example:

```bash
sudo usermod -U john
```

This command unlocks the previously locked user account named "john."



-----


## Understanding Home Directory:

A home directory is a user's personal workspace where files, settings, and configurations are stored. It is associated with a specific user account and is crucial for user-specific customization and data storage. The home directory is usually located at `/home/username` in Linux.

-----

# Default Group in User Creation on Linux

When you create a user on a Linux system using the `useradd` command, a default group for that user is indeed created. This default group is often named after the user and serves as the user's primary group. The user is automatically added to this primary group, and it's the group that's associated with the user's initial login session.

Here's how it typically works:

1. **Default Group Naming Convention:**
   - The default group is created with the same name as the user by default.
   - For example, if you create a user named "john," a group named "john" will be created as well.

2. **Primary Group Assignment:**
   - The user is automatically added to their default group as the primary group.
   - When the user logs in, this group is set as the primary group for the user.

3. **Group ID (GID):**
   - A unique Group ID (GID) is assigned to the default group.
   - This GID is associated with both the group and the user.

4. **Group Membership:**
   - The user is initially a member of only their default group.
   - Additional groups can be assigned to the user using the `-G` option with the `useradd` command.

Here's a simple example using the `useradd` command:

```bash
sudo useradd john
```

In this example:
- A user named "john" is created.
- A group named "john" is automatically created.
- "john" is added to the "john" group.
- "john" is the primary group for the user "john."

You can view the user's details, including the primary group, by using the `id` command:

```bash
id john
```

The output will include information about the user's UID (User ID), GID (Group ID), and groups:

```bash
uid=1001(john) gid=1001(john) groups=1001(john)
```

This indicates that the user "john" has a UID and GID of 1001, and the primary group is "john." The "groups" section shows additional groups if the user belongs to any supplementary groups.

This default group simplifies user management by automatically associating a user with a group of the same name during account creation.


--------

:


# Overview of Key Linux System Files: `/etc/passwd` , `/etc/shadow`, `/etc/group`

## 1. `/etc/passwd` File:

### Purpose:
The `/etc/passwd` file is a text-based database that stores essential information about user accounts on a Linux system. Each line in this file represents a user account and contains various fields separated by colons (`:`).

### Fields:
1. **Username (Login name):** The name used to log in.
2. **Password Placeholder (x):** In the past, the encrypted password used to be stored here, but now it's typically an 'x,' indicating that the password is stored in the `/etc/shadow` file.
3. **User ID (UID):** A unique numerical identifier for the user.
4. **Group ID (GID):** The primary group ID for the user.
5. **User Info (GECOS):** Additional information about the user (e.g., full name, phone number).
6. **Home Directory:** The absolute path to the user's home directory.
7. **Login Shell:** The default shell for the user.

### Example Line:
```plaintext
john:x:1001:1001:John Doe:/home/john:/bin/bash
```

## 2. `/etc/shadow` File:

### Purpose:
The `/etc/shadow` file stores the encrypted password information for user accounts. It is a security-enhanced version of the `/etc/passwd` file. User passwords and related information, such as password expiration, are stored here.

### Fields:
1. **Username:** The same as in `/etc/passwd`.
2. **Encrypted Password:** The hashed and encrypted password.
3. **Last Password Change:** The number of days since the password was last changed.
4. **Password Expiry:** The number of days after which the password must be changed.
5. **Password Inactivity:** The number of days of inactivity allowed before the account is locked.
6. **Account Expiry:** The number of days after which the account is disabled.

### Example Line:
```plaintext
john:$6$KVuXoJU1$UaHgfz1F4HJtSDqat8KluQFNO2dbkKHUxSYZYuTAb7sU:18614:0:99999:7:::
```

## 3. `/etc/group` File:

### Purpose:
The `/etc/group` file contains information about groups on the system. Each line represents a group and includes details such as the group name, group password (rarely used), group ID (GID), and a list of users who are members of the group.

### Fields:
1. **Group Name:** The name of the group.
2. **Group Password:** Historically used for an encrypted password for the group (rarely used nowadays).
3. **Group ID (GID):** The numerical identifier for the group.
4. **Group Members:** A comma-separated list of users who are members of the group.

### Example Line:
```plaintext
developers:x:1001:john,jane,bob
```

### Summary:
- `/etc/passwd`: User account information.
- `/etc/shadow`: Encrypted password information.
- `/etc/group`: Group information.

Understanding these files is crucial for managing user accounts and groups on a Linux system. The permissions for these files are restricted to root to ensure their security.

