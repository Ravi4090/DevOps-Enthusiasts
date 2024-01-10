
# User and Group Management in Linux

Linux user and group management involves creating, modifying, and organizing user accounts and groups on a Linux system. This process is crucial for controlling access to resources, ensuring security, and simplifying system administration.



## Contents

- What are Users in Linux ?

- Types of Users in Linux ?

- User Account Properties ?

- How to Create Users ?

- How to Delete Users ?

- How to Modify User Accounts ?

- Password Management ?

- Group Management ?

-------

## What are Users in Linux ?

In a Linux system, users refer to individuals or entities that interact with the operating system by logging in and performing various tasks. User management plays a crucial role in ensuring secure access control, resource allocation, and system administration.

A user in Linux is associated with a user account, which consists of several properties defining their identity and privileges within the system. These properties are a username, UID (User ID), GID (Group ID), home directory, default shell, and password.

Each user account possesses these unique properties listed above.

----
## Types of Users in Linux 

### System Users:

Definition: System users are accounts created by the operating system during the installation process. These accounts are dedicated to running system services, daemons, and background processes that are essential for the proper functioning of the operating system.

Purpose: System users exist to handle specific tasks or services required by the operating system. They typically do not represent individual human users interacting directly with the system.

Examples: Some examples of system users include accounts associated with services like web servers (e.g., Apache or Nginx), databases (e.g., MySQL or PostgreSQL), and system processes.

### Regular Users:

Definition: Regular users, also known as normal or standard users, are accounts created by administrators or users themselves for human interaction with the system. These accounts are meant for individuals who log in, perform tasks, and use the system's resources.

Purpose: Regular users have varying levels of permissions and can execute commands, access files, and perform tasks based on their assigned privileges. They interact with the system directly, running applications, managing personal files, and performing day-to-day activities.

Examples: Users like developers, system administrators, or end-users who utilize the system for work or personal tasks are examples of regular users.

### Key Differences:

Creation: System users are automatically created during the system installation, while regular users are manually created by administrators or users themselves.

Roles: System users handle background processes and services critical for system functionality, while regular users interact directly with the system for various purposes.

Permissions: System users often have elevated privileges to perform specialized system-level tasks, while regular users have permissions based on their assigned roles and responsibilities.

Examples: System users are associated with specific services, whereas regular users represent individuals with distinct roles in the organization or community.

In summary, system users are instrumental for the smooth operation of the operating system itself, handling background processes and services, while regular users are human users who interact with the system for diverse tasks and activities.

-----
## How to Create Users in Linux

Lets consider Arjun, needs to create user accounts for Aryan, Lata, and Sneha. Arjun initiates the process using the useradd command. For example, to create Aryan's account, Arjun executes the command below: 
```bash
  useradd -u 1002 -d /home/aryan -s /bin/bash aryan
```

This command creates Aryan's account with uid (-u) as 1002, the home directory (-d) as /home/aryan and sets (-s) /bin/bash as his default shell.

Arjun can verify the new user account by running the id command:
```bash
  id aryan
```

Similarly, Arjun will create a user account for Lata and Sneha using the same format.


```bash
  useradd -u 1003 -d /home/lata -s /bin/bash lata
```

This command creates Lata's account with uid (-u) as 1003, the home directory (-d) as /home/lata, and sets (-s) /bin/bash as her default shell.


```bash
  useradd -u 1004 -d /home/sneha -s /bin/bash sneha
```

This command creates Sneha's account with uid (-u) as 1004, the home directory (-d) as /home/sneha, and sets (-s) /bin/bash as her default shell.

-----
## User Account Properties In Linux

User accounts possess various properties that define their characteristics and access privileges. Let's explore these properties in the context of our use case.

### Username:
Each user is assigned a unique username that serves as their identifier within the Linux system. For example, Arjun's username is "arjun".

### UID (User ID) and GID (Group ID):
Every user account is associated with a UID and GID. The UID is a numerical value assigned to the user, while the GID represents the primary group to which the user belongs. For instance, Arjun's UID may be 1002, and his primary group's GID is 1002 as well.

### Home Directory:
Each user has a designated home directory where their personal files and settings reside. Arjun's home directory is /home/arjun.

### Default Shell:
The default shell determines the command interpreter used when a user logs in. It defines the user's interactive environment. In our case, Arjun's default shell is set to /bin/bash, which is a popular shell in Linux.

### Password:
User accounts require passwords to authenticate and access the system. All users, including Arjun, must create strong passwords to ensure security.

### Group:
The group membership determines which system resources the user can access, as well as which users can access the user's files.

Arjun could take a look at the users on their Linux by running the cat **/etc/passwd** command. The users will be displayed in this format:

```bash
arjun:x:1002:1002:,,,:/home/arjun:/bin/bash
```
Here's what each of the fields in the format above represents:

**arjun**: This is the username of the user account.

**x**: This field contains the encrypted password of the user. It is replaced with an 'x' character to indicate that the password is stored in the /etc/shadow file for security reasons.

**1002**: This is the UID (User ID) of the user account, which is a unique numerical identifier assigned to the user by the system.

**1002**: This is the GID (Group ID) of the user account, which represents the primary group membership of the user.

**,,,:** This is the GECOS field, which stands for "General Electric Comprehensive Operating System". This field is used to store additional information about the user, such as their full name or contact information. In this case, the field is empty, as no additional information was provided while creating the user account.

**/home/arjun:** This is the home directory of the user account, which is the location where the user's files and personal data are stored.

**/bin/bash:** This is the default shell for the user account, which is the command interpreter used to process commands entered by the user in the terminal. In this case, the default shell is Bash, which is the most commonly used shell in Linux.


-------------------------------------------------

## How to Delete Users 

Let's assume that Lata has left Company. To remove her account and associated files, Arjun has to utilize the userdel command. For instance, to delete Lata's account, Arjun runs:

```bash
sudo userdel lata
```

This will delete the user account for lata, along with their home directory and any files or directories owned by the user.



-----
## How to Modify User Accounts

#### How to Change Default Shell in Linux:

In a case where Aryan prefers to use a different shell other than the default /bin/bash shell, the IT team can modify his account accordingly. For example, to change Aryan's default shell to /bin/zsh, the following command can be used:

```bash
sudo usermod -s /bin/zsh aryan
```

This command updates Aryan's account to use the new default shell — /bin/zsh.

You can run the cat **/etc/passwd** again to see that the shell for aryan has changed from /bin/bash to /bin/zsh.

#### Modifying User's Home Directory

In a case where we want to the change the latha Home Directory to some thing else in place of default home Directory

```
sudo usermod -d /new/home/structure latha
```

Explanation:
This command changes Latha's home directory to the specified path.

#### Modifying Users Full Name (GECOS field):

In a case where we want to the change the Latha's Full Name in the (GECOS field) 

```
sudo usermod -c "New Full Name" 
```

Explanation:
This command updates the GECOS field for Latha, providing additional information like her full name.

---
#### Modifying Password Expiry for User Account


The chage command is used to modify user password expiration settings. In this specific command, -d 0 sets the password expiration date to "0," meaning it's immediately expired.




```bash
sudo chage -d 0 latha
```

This sets the password expiry for Latha, forcing her to change the password at the next login.

---

#### Locking/Unlocking an User Account 


This command locks Latha's user account, preventing her from logging in. It is a security measure typically employed when there are concerns about unauthorized access or suspicious activity associated with the account.


```bash
  sudo usermod -L latha
```


Conversely, this command unlocks Latha's user account, restoring her ability to log in. Unlocking is done when the security concern that led to the account lockout has been resolved, and Latha should regain access.

```bash
  sudo usermod -U latha
```

These actions are often taken in response to security policies or specific circumstances requiring adjustments to user account access and authentication. Always ensure that such changes are made in accordance with organizational policies and with proper authorization.


## Password Management 

Implementing robust password management practices is crucial to uphold the security of user accounts within the Any Companies Linux environment. Let's delve into how the IT team can institute stringent password policies and efficiently handle user passwords


**Establishing Password Policies:**

The IT team has the capability to define password policies, ensuring the adoption of strong passwords. These policies encompass requirements for complexity, password expiration, and account lockouts. The configuration of these policies is carried out in the /etc/login.defs file.


**Encouraging Password Changes:**

Users are advised to periodically update their passwords to enhance security. This can be achieved by utilizing the passwd command. As an illustration, John can modify his password by executing the following command:



```bash
 sudo passwd john
```

Executing this command initiates a prompt for John to input his existing password and subsequently empowers him to establish a new, robust password. This proactive approach to password management contributes significantly to reinforcing the overall security posture of the system.
