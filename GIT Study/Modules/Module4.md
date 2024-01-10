# Module 4 : Installation and Setting up Git

-----

Installing Git on various operating systems is a straightforward process. Here are instructions for different operating systems:

-----

### **1. Amazon EC2 (Amazon Linux):**

Connect to your Amazon EC2 instance using SSH, and then run the following commands:

```bash
sudo yum update
sudo yum install git
```

This will update your package information and install Git on your Amazon Linux EC2 instance.


----

### **2. Ubuntu:**

On Ubuntu, you can use the package manager to install Git. Open a terminal and run the following commands:

```bash
sudo apt update
sudo apt install git
```

This will update your package information and install Git on your Ubuntu system.

----

### **3. Windows:**

For Windows, you can use the Git Bash terminal, which provides a Unix-like command-line environment.

1. Download the Git for Windows installer from the official Git website: [Git for Windows](https://gitforwindows.org/).
   
2. Run the installer, following the on-screen instructions. The default settings are usually sufficient.

3. During the installation, you can choose the default editor and the terminal emulator to use with Git.

4. Once the installation is complete, you can open the Git Bash terminal from the Start menu.

----

### **4. macOS:**

Git is usually pre-installed on macOS. However, you can update it to the latest version using the following commands in the terminal:

```bash
brew update
brew install git
```

This assumes you have Homebrew installed. If not, you can install it by following the instructions on the [Homebrew website](https://brew.sh/).

After these installations, you can verify that Git is installed by running:

```bash
git --version
```

This should display the installed Git version on your system.

Remember that the commands above assume you have the necessary permissions to install software on your system. If you encounter any issues, you might need to use `sudo` on Linux systems or run the installer with administrator privileges on Windows.
