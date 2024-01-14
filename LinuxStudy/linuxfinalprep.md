
| S.No | Command                   | Syntax                                         | Description                                     | Example                                              |
|------|---------------------------|------------------------------------------------|-------------------------------------------------|------------------------------------------------------|
| 1    | `mkdir`                   | `mkdir [directory_name]`                       | Create a new directory.                         | `mkdir new_directory`                                |
| 2    | `ls`                      | `ls [options] [path]`                          | List files and directories in the current path. | `ls -l /home/user`                                   |
| 3    | `cd`                      | `cd [directory]`                               | Change the current working directory.           | `cd Documents`                                       |
| 4    | `touch`                   | `touch [filename]`                             | Create an empty file or update timestamp.      | `touch newfile.txt`                                  |
| 5    | `cat`                     | `cat [filename]`                               | Display the contents of a file.                | `cat example.txt`                                    |
| 6    | `cat >newfile.txt`        | `cat > [filename]`                             | Create a new file and write into it.           | `cat >newfile.txt`                                   |
| 7    | `cat file1 file2 > file3` | `cat [file1] [file2] > [file3]`                | Concatenate files and redirect output.         | `cat file1.txt file2.txt > mergedfile.txt`          |
| 8    | `pwd`                     | `pwd`                                          | Print the current working directory.           | `pwd`                                                |
| 9    | `cp`                      | `cp [options] source destination`              | Copy files and directories.                    | `cp file.txt /backup`                                |
| 10   | `mv`                      | `mv [options] source destination`              | Move/rename files and directories.             | `mv file.txt new_location/`                          |
| 11   | `head`                    | `head [options] [file]`                        | Display the first lines of a file.             | `head -n 10 example.txt`                             |
| 12   | `tail`                    | `tail [options] [file]`                        | Display the last lines of a file.              | `tail -n 20 example.log`                             |
| 13   | `tac`                     | `tac [file]`                                   | Display a file's content in reverse.           | `tac example.txt`                                    |
| 14   | `less`                    | `less [file]`                                  | View file content with page-by-page navigation.| `less long_file.txt`                                 |
| 15   | `id`                      | `id [username]`                                | Display user and group information.            | `id john`                                            |
| 16   | `clear`                   | `clear`                                        | Clear the terminal screen.                      | `clear`                                              |
| 17   | `vi`                      | `vi [filename]`                               | Open a text editor.                            | `vi document.txt`                                    |
| 18   | `grep`                    | `grep [options] pattern [file]`               | Search for a pattern in a file.                | `grep "error" log.txt`                               |
| 19   | `diff`                    | `diff file1 file2`                            | Compare two files line by line.               | `diff file1.txt file2.txt`                           |
| 20   | `ping`                    | `ping [hostname or IP]`                       | Check network connectivity to a host.         | `ping google.com`                                    |
| 21   | `history`                 | `history`                                      | Display a list of recently executed commands. | `history`                                           |
| 22   | `rm`                      | `rm [options] [file]`                         | Remove/delete files or directories.           | `rm file.txt`                                        |
| 23   | `rmdir`                   | `rmdir [directory]`                           | Remove an empty directory.                     | `rmdir empty_directory`                              |
| 24   | `uniq`                    | `uniq [options] [file]`                       | Report or omit repeated lines.                | `uniq sorted_file.txt`                               |
| 25   | `wc`                      | `wc [options] [file]`                         | Count lines, words, and characters in a file. | `wc -l document.txt`                                |
| 26   | `hostname`                | `hostname`                                    | Display the system's hostname.                 | `hostname`                                           |
| 27   | `hostname -i`             | `hostname -i`                                 | Display the system's IP address.               | `hostname -i`                                        |
| 28   | `uname`                   | `uname [options]`                             | Display system information.                   | `uname -a`                                           |
| 29   | `whoami`                  | `whoami`                                      | Display the current username.                 | `whoami`                                             |
| 30   | `apropos`                 | `apropos [keyword]`                           | Search the manual page names and descriptions.| `apropos search_term`                                |
| 32   | `netstat`                 | `netstat [options]`                           | Display network connections and routing tables. | `netstat -an`                                      |
| 34   | `ps`                      | `ps [options]`                                | Display information about a selection of the active processes. | `ps aux`                                           |
| 35   | `who`                     | `who [options]`                              | Show who is logged on.                        | `who`                                               |
| 36   | `env`                     | `env`                                         | Display environment variables.                | `env`                                               |
| 37   | `lsblk`                   | `lsblk [options]`                            | List information about block devices.         | `lsblk`                                             |
| 38   | `lsusb`                   | `lsusb [options]`                            | List USB devices.                            | `lsusb`                                             |
| 39   | `lsof`                    | `lsof [options] [file]`                      | List open files.                            | `lsof /var/log/syslog`                               |
| 40   | `lspci`                   | `lspci [options]`                            | List all PCI devices.                       | `lspci`                                             |
| 41   | `wget`                    | `wget [options] [URL]`                       | Download files from the web.                | `wget http://example.com/file.zip`                   |
| 43   | `tee`                     | `tee [options] [file]`                       | Redirect output to multiple files.         | `echo "Hello" | tee output.txt`                            |
| 44   | `cut`                     | `cut [options] [file]`                       | Remove sections from each line of a file.  | `cut -d',' -f2 data.csv`                              |
| 45   | `awk`                     | `awk [options] 'pattern { action }' [file]` | A versatile programming language for text processing. | `awk '/pattern/ {print $1}' data.txt`              |
| 46   | `sed`                     | `sed [options] 'script' [file]`              | Stream editor for filtering and transforming text. | `sed 's/old/new/g' file.txt`                        |
| 47   | `chown`                   | `chown [options] [user:group] [file]`       | Change file owner and group.                | `chown user:group file.txt`                         |
| 48   | `df`                      | `df [options] [file]`                        | Report file system disk space usage.       | `df -h`                                             |
| 49   | `du`                      | `du [options] [directory]`                   | Estimate file space usage.                  | `du -sh /path/to/directory`                         |
| 50   | `free`                    | `free [options]`                             | Display amount of free and used memory in the system. | `free -h`                                       |
| 51   | `top`                     | `top`                                        | Display and update sorted information about system processes. | `top`                                        |
| 52   | `tar`                     | `tar [options] [file or directory]`         | Create, list, extract files from an archive. | `tar -cvf archive.tar.gz source_directory`          |
| 55   | `exit`                    | `exit`                                       | Exit the current shell session.             | `exit`                                              |
| 56   | `date`                    | `date [options]`                            | Display or set the date and time.           | `date`                                              |
| 57   | `cal`                     | `cal [options]`                             | Display a calendar.                        | `cal`                                               |
| 58   | `uptime`                  | `uptime`                                    | Display how long the system has been running. | `uptime`                                          |
| 59   | `cat /proc/cpuinfo`       | `cat /proc/cpuinfo`                         | Display detailed CPU information.          | `cat /proc/cpuinfo`                                |
| 60   | `cat /proc/meminfo`       | `cat /proc/meminfo`                         | Display information about system memory.   | `cat /proc/meminfo`                                 |
| 61   | `chmod`                   | `chmod [options] mode file`                  | Change file mode (permissions).             | `chmod 755 script.sh`                               |
