
# `diff` Command in Linux

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


