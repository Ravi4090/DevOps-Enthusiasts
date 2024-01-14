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

## DF COMMAND

- **`df` - Disk Free:**
  - Displays disk space information.
  - Options like `-h` provide human-readable sizes.
  - Helps check available space, usage percentages, and filesystem details.

## DU COMMAND

- **`du` - Disk Usage:**
  - Estimates file space usage for files and directories.
  - Options like `-h` provide human-readable sizes.
  - Useful for determining disk space usage in specific locations.

## FREE COMMAND (RAM)

- **`free` - Display Amount of Free and Used Memory:**
  - Shows information about free and used physical and swap memory.
  - Options like `-m` display values in megabytes.
  - Monitors system memory usage.

------

-----






# Grep Command Overview

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




# Byte-by-Byte Comparison with `cmp` Command

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

This breakdown shows the comparison at each byte position and identifies where the first difference occurs (byte 5) in line 3 of the files.

If you have further questions or need more clarification, feel free to ask!
