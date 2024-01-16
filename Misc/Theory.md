# Linux Command Overview

## 1. DATE COMMAND

### Options:

- **Current Year:** `date "+%Y"` - Displays the current year in a four-digit format.
- **Current Month:** `date "+%m"` - Displays the current month in two digits (01 for January, 02 for February, etc.).
- **Current Day:** `date "+%d"` - Displays the current day of the month.
- **Day Name (Small Form):** `date "+%b"` - Displays the abbreviated day name (e.g., Mon, Tue).
- **Day Name (Full Form):** `date "+%A"` - Displays the full day name (e.g., Monday, Tuesday).
- **Month Name (Small Form):** `date "+%a"` - Displays the abbreviated month name (e.g., Jan, Feb).
- **Month Name (Full Form):** `date "+%B"` - Displays the full month name (e.g., January, February).
- **Time (Hours):** `date "+%H"` - Displays the current hour in 24-hour format.
- **Time (Minutes):** `date "+%M"` - Displays the current minute.
- **Time (Seconds):** `date "+%S"` - Displays the current second.
- **Formatting Time:** `date "+%H:%M:%S"` - Displays the current time in HH:MM:SS format.

### Example Explanation:

- The output `Fri Jan 12 22:03:27 UTC 2024` represents Friday, January 12, 2024, at 22:03:27 (10:03:27 PM) in Coordinated Universal Time (UTC).

## 2. UPTIME COMMAND

- The `uptime` command provides information about the system's uptime, number of users, and load averages.
- The output `22:08:42 up 2 days, 15:31,  1 user,  load average: 0.00, 0.01, 0.00` breaks down as follows:
  - Current time: 22:08:42
  - System uptime: 2 days, 15 hours, and 31 minutes.
  - Number of users: 1
  - Load averages over the last 1, 5, and 15 minutes: 0.00, 0.01, 0.00.
- Load averages represent the average number of processes in the system's run queue over the specified time intervals.

## 3. MORE AND LESS COMMANDS

- **more Command:**
  - Basic pager for viewing text one screen at a time.
  - Forward navigation only.
  - Simple and suitable for quick file viewing.

- **less Command:**
  - Enhanced pager with forward and backward navigation.
  - Allows scrolling, searching, and interactive features.
  - More user-friendly for viewing large files.

## 4. CAL COMMAND

- **Specific Year:** `cal 2024` - Displays the calendar for the entire year 2024.
- **Specific Month of a Year:** `cal 6 2024` - Displays the calendar for June 2024.
- **Previous Year:** `cal 2020` - Displays the calendar for the entire year 2020.
- **Previous, Current, and Next Month:** `cal -3` - Displays the calendars for the previous, current, and next month.
- **Entire Calendar of the Current Year:** `cal -y` - Displays the entire calendar of the current year.
- **Display Specific Month in Current Year:** `cal -m 6` - Displays the calendar for June in the current year.

## 5. SORT COMMAND

- **Ascending Sort:** `sort file.txt` - Sorts lines in ascending order.
- **Descending/Reverse Sort:** `sort -r file.txt` - Sorts lines in descending order.
- **Sorting Multiple Files:** `sort file1.txt file2.txt` - Sorts lines from multiple files.
- **Numbers Sorting:** `sort -n numbers.txt` - Sorts lines treating them as numbers.

## 6. UNIQUE COMMAND

- **Data Without Duplicates:** `sort file.txt | uniq` - Displays unique lines from a sorted file.
- **Data with Repeated Entries:** `sort file.txt | uniq -d` - Displays only repeated lines.
- **Data Without Repeated Entries:** `sort file.txt | uniq -u` - Displays only unique lines.
- **Count of Repeated Entries:** `sort file.txt | uniq -c` - Displays the count of each repeated entry.

## WHAT IS A FILE SYSTEM

- A file system organizes and stores data on a storage device.
- It provides a structure for naming, storing, and retrieving files.
- Manages data storage, retrieval, and access by the operating system and applications.

## 7. DF COMMAND

- **`df` - Disk Free:**
  - Displays disk space information.
  - Options like `-h` provide human-readable sizes.
  - Helps check available space, usage percentages, and filesystem details.

## 8. DU COMMAND

- **`du` - Disk Usage:**
  - Estimates file space usage for files and directories.
  - Options like `-h` provide human-readable sizes.
  - Useful for determining disk space usage in specific locations.

## 9. FREE COMMAND (RAM)

- **`free` - Display Amount of Free and Used Memory:**
  - Shows information about free and used physical and swap memory.
  - Options like `-m` display values in megabytes.
  - Monitors system memory usage.

## 10.  Grep Command 

Let's explore each of the `grep` options you mentioned with detailed explanations and examples using a sample file. Assume we have a file named `sample.txt` with the following content:

```plaintext
apple
banana
cherry
date
kiwi
orange
grape
pineapple
```

Now, let's explore each option:

## 1. `-c` (Count Matching Lines):

```bash
grep -c "a" sample.txt
```

- **Explanation:**
  - Counts and prints the number of lines that contain the specified pattern ("a").

- **Output:**
  ```plaintext
  5
  ```

  - There are five lines in the file that contain the letter "a."

## 2. `-h` (Suppress Filename Prefix):

```bash
grep -h "a" sample.txt
```

- **Explanation:**
  - Suppresses the display of filenames when searching multiple files.

- **Output:**
  ```plaintext
  apple
  banana
  date
  grape
  ```

  - Displays only the lines containing the letter "a" without showing the filenames.

## 3. `-i` (Case-Insensitive Search):

```bash
grep -i "kiWi" sample.txt
```

- **Explanation:**
  - Performs a case-insensitive search for the pattern ("kiWi").

- **Output:**
  ```plaintext
  kiwi
  ```

  - Displays the line containing "kiwi" regardless of letter case.

## 4. `-n` (Display Line Numbers):

```bash
grep -n "e" sample.txt
```

- **Explanation:**
  - Displays line numbers along with the matched lines containing the pattern ("e").

- **Output:**
  ```plaintext
  1: apple
  5: kiwi
  ```

  - Shows line numbers for lines containing the letter "e."

## 5. `-v` (Invert Match):

```bash
grep -v "a" sample.txt
```

- **Explanation:**
  - Inverts the match, displaying lines that do not contain the pattern ("a").

- **Output:**
  ```plaintext
  cherry
  date
  kiwi
  orange
  grape
  pineapple
  ```

  - Displays lines that do not contain the letter "a."

## 6. `-o` (Display Matching Part Only):

```bash
grep -o "ra" sample.txt
```

- **Explanation:**
  - Displays only the matching part of the line containing the pattern ("ra").

- **Output:**
  ```plaintext
  ra
  ```

  - Shows the matching part "ra" from the lines containing it.

## 7. `-e` (Specify Multiple Patterns):

```bash
grep -e "a" -e "kiwi" sample.txt
```

- **Explanation:**
  - Searches for multiple patterns ("a" and "kiwi") within the same file.

- **Output:**
  ```plaintext
  apple
  kiwi
  ```

  - Displays lines containing either "a" or "kiwi."

## 8. `^` (Match Lines Starting with):

```bash
grep "^p" sample.txt
```

- **Explanation:**
  - Matches lines that start with the specified pattern ("p").

- **Output:**
  ```plaintext
  pineapple
  ```

  - Displays the line starting with the letter "p."

## 9. `$` (Match Lines Ending with):

```bash
grep "e$" sample.txt
```

- **Explanation:**
  - Matches lines that end with the specified pattern ("e").

- **Output:**
  ```plaintext
  apple
  orange
  grape
  pineapple
  ```

  - Displays lines ending with the letter "e."

## 10. `i` (Whole Word Match):

```bash
grep -w "a" sample.txt
```

- **Explanation:**
  - Ensures that only whole words (not substrings) are matched.

- **Output:**
  ```plaintext
  banana
  grape
  ```

  - Displays lines where "a" is a whole word, not part of another word.

 ----




## 11. Byte-by-Byte Comparison with `cmp` Command

Let's break down the byte-by-byte comparison for the provided files:

## Command

```bash
[ec2-user@ip-172-31-6-126 ~]$ cmp cmpone.txt cmptwo.txt
cmpone.txt cmptwo.txt differ: byte 5, line 3
```

- **Explanation:**
  - The `cmp` command is used to compare the contents of `cmpone.txt` and `cmptwo.txt`.
  - It reports that the files differ at byte 5, line 3.

```bash
[ec2-user@ip-172-31-6-126 ~]$ cat cmpone.txt
A
B
C
D
F
[ec2-user@ip-172-31-6-126 ~]$ cat cmptwo.txt
A
B
M
D
G
```

- **File Contents:**
  - **`cmpone.txt`:**
    ```
    A
    B
    C
    D
    F
    ```

  - **`cmptwo.txt`:**
    ```
    A
    B
    M
    D
    G
    ```

- **Byte-by-Byte Comparison:**
  - Byte 1: A (in both files)
  - Byte 2: Newline character (in both files)
  - Byte 3: B (in both files)
  - Byte 4: Newline character (in both files)
  - Byte 5: C (in `cmpone.txt`), M (in `cmptwo.txt`) - **First difference**
  - Byte 6: Newline character (in both files)
  - Byte 7: D (in `cmpone.txt`), N (in `cmptwo.txt`)

- **Interpretation:**
  - The files start with the same content until byte 5, where they differ.
  - The content at byte 5 in `cmpone.txt` is "C," while in `cmptwo.txt` it is "M."
  - The difference is detected in line 3 of the files.

This breakdown shows the comparison at each byte position and identifies where the first difference occurs (byte 5) in line 3 of the files.!

---------------------




## 12. Introduction to `sed` (Stream Editor)

The `sed` command (stream editor) is a powerful tool for text stream processing. It is often used for non-interactive text transformations, such as search and replace, deletion, insertion, and more.

## `sed` Command Syntax:

```bash
sed OPTIONS... [SCRIPT] [INPUTFILE...]
```

Some common `sed` commands include:

- `s/old/new/g`: Substitutes all occurrences of "old" with "new" in each line.
- `d`: Deletes lines.
- `p`: Prints lines.
- `i`: Inserts text before a line.
- `a`: Appends text after a line.

Now, let's demonstrate a basic usage of `sed`.

Suppose you have a file named `example.txt` with the following content:

```plaintext
Hello, World!
This is a demonstration.
```

You can use `sed` to replace "Hello" with "Hi" and print the modified content:

```bash
sed 's/Hello/Hi/' example.txt
```

**Explanation:**

- `s/Hello/Hi/`: Substitutes "Hello" with "Hi".
- `example.txt`: Input file.

**Output:**
```plaintext
Hi, World!
This is a demonstration.
```

This basic example showcases how `sed` can be used for simple text transformations. The `sed` command provides a flexible and efficient way to process text streams in a variety of scenarios.

---------------

# `sed` Examples

Let's go through each `sed` example in detail.

## 1. Search and Replace:

```bash
sed 's/Hello/Hi/' example.txt
```

- `s/Hello/Hi/`: This is the substitution command in `sed`. It searches for the pattern "Hello" and replaces it with "Hi".
- `example.txt`: This is the input file.

**Output:**
```plaintext
Hi, World!
This is a demonstration.
```

## 2. Delete Lines:

```bash
sed '/This/d' example.txt
```

- `/This/`: This is a pattern to match lines containing the word "This".
- `d`: This is the delete command. It deletes lines that match the specified pattern.

**Output:**
```plaintext
Hello, World!
```

## 3. Print Specific Lines:

```bash
sed -n '2p' example.txt
```

- `-n`: This option suppresses the default output, and only lines explicitly selected for printing are displayed.
- `2p`: This command prints the second line.

**Output:**
```plaintext
This is a demonstration.
```

## 4. Insert Text:

```bash
sed '2i\Inserted Line' example.txt
```

- `2i\`: This command inserts text before the specified line number (line 2 in this case).
- `Inserted Line`: This is the text to be inserted.

**Output:**
```plaintext
Hello, World!
Inserted Line
This is a demonstration.
```

## 5. Append Text:

```bash
sed '2a\Appended Line' example.txt
```

- `2a\`: This command appends text after the specified line number (line 2 in this case).
- `Appended Line`: This is the text to be appended.

**Output:**
```plaintext
Hello, World!
This is a demonstration.
Appended Line
```

These `sed` commands demonstrate basic text transformations, including search and replace, line deletion, printing specific lines, inserting text, and appending text. Each command performs a specific action on the input file, showcasing the flexibility and power of the `sed` tool for text processing.


----------------------




## 13. `diff` Command in Linux

The `diff` command in Linux is used to compare the contents of two text files line by line and display the differences. Below are some important options of the `diff` command explained with a simple example:

## Example Files:
Let's consider two text files: `file1.txt` and `file2.txt`.

**`file1.txt`:**
```plaintext
This is line 1.
This is line 2.
This is line 3.
```

**`file2.txt`:**
```plaintext
This is line 1.
This is a modified line.
This is line 3.
```

## 1. Basic Usage:
```bash
diff file1.txt file2.txt
```

**Output:**
```plaintext
2c2
< This is line 2.
---
> This is a modified line.
```

**Explanation:**
- `2c2`: Indicates a change in the second line.
- `< This is line 2.`: Original content in `file1.txt`.
- `---`: Separator.
- `> This is a modified line.`: Modified content in `file2.txt`.



## 2. Side-by-Side Format (-y):
```bash
diff -y file1.txt file2.txt
```

**Output:**
```plaintext
This is line 1.                              | This is line 1.
This is line 2.                              | This is a modified line.
This is line 3.                              | This is line 3.
```

**Explanation:**
- `-y`: Presents a side-by-side comparison.
- `|`: Separates the lines from the two files.

## 3. Ignore Whitespace Changes (-w):
```bash
diff -w file1.txt file2.txt
```

**Output:**
```plaintext
2c2
< This is line 2.
---
> This is a modified line.
```

**Explanation:**
- `-w`: Ignores whitespace changes.
----


