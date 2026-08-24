# 01 — File Management

This section covers basic Linux commands used to navigate, create, copy, move, remove, search, and identify files and directories.

These commands are fundamental for working with the Linux command line and are useful in system administration, troubleshooting, and cybersecurity.

## Commands Covered

### 1. `pwd` — Print Working Directory

Displays the full path of the directory you are currently working in.

```bash
pwd
```

**Example:**

```bash
pwd
```

**Use case:**
Useful for confirming your current location in the filesystem before performing file operations.

---

### 2. `ls` — List Directory Contents

Displays files and directories in the current location.

```bash
ls
```

**Useful options:**

```bash
ls -l
ls -a
ls -la
```

* `-l` — Displays detailed information.
* `-a` — Shows hidden files.
* `-la` — Shows hidden files with detailed information.

**Use case:**
Useful for inspecting directories and identifying files, including hidden files.

---

### 3. `cd` — Change Directory

Used to move from one directory to another.

```bash
cd directory_name
```

**Examples:**

```bash
cd Documents
cd ..
cd ~
```

* `cd ..` — Moves to the parent directory.
* `cd ~` — Returns to the user's home directory.

**Use case:**
Essential for navigating through the Linux filesystem.

---

### 4. `mkdir` — Make Directory

Creates a new directory.

```bash
mkdir directory_name
```

**Example:**

```bash
mkdir linux-lab
```

**Use case:**
Useful for organizing files, projects, scripts, and investigation data.

---

### 5. `touch` — Create a File

Creates an empty file or updates the timestamp of an existing file.

```bash
touch filename
```

**Example:**

```bash
touch notes.txt
```

**Use case:**
Useful for creating files from the terminal, such as notes, scripts, or temporary files.

---

### 6. `cp` — Copy Files

Copies files or directories to another location.

```bash
cp source destination
```

**Example:**

```bash
cp notes.txt backup.txt
```

**Use case:**
Useful for creating backups or making copies of files before modifying them.

---

### 7. `mv` — Move or Rename

Moves files or directories or changes their names.

```bash
mv source destination
```

**Example:**

```bash
mv notes.txt linux-notes.txt
```

This renames `notes.txt` to `linux-notes.txt`.

**Use case:**
Useful for organizing files and moving files between directories.

---

### 8. `rm` — Remove Files

Deletes files.

```bash
rm filename
```

**Example:**

```bash
rm linux-notes.txt
```

**Important:**
Be careful when using `rm` because deleted files may not be recoverable through normal means.

**Use case:**
Useful for removing unnecessary or temporary files.

---

### 9. `find` — Search for Files

Searches for files and directories based on different criteria.

```bash
find location -name "filename"
```

**Example:**

```bash
find . -name "notes.txt"
```

The `.` means to search from the current directory.

**Use case:**
Useful during system administration and security investigations when looking for specific files or file types.

---

### 10. `file` — Identify File Type

Determines the type of a file.

```bash
file filename
```

**Example:**

```bash
file notes.txt
```

**Use case:**
Useful when investigating unfamiliar or suspicious files to determine what type of file they actually are.

---

## Practical Exercise

The following commands were used to practice basic file management:

```bash
mkdir linux-lab
cd linux-lab
touch notes.txt
ls
cp notes.txt backup.txt
mv backup.txt backup-notes.txt
find . -name "notes.txt"
file notes.txt
rm backup-notes.txt
```

This exercise demonstrates how files and directories can be created, viewed, copied, renamed, searched, identified, and removed from the Linux terminal.

## Cybersecurity Relevance

File management is a fundamental skill for cybersecurity professionals working with Linux systems.

Security analysts and system administrators regularly need to:

* Navigate unfamiliar filesystems.
* Locate specific files.
* Identify suspicious files.
* Create backups of important files.
* Organize investigation evidence.
* Remove unnecessary or temporary files.

Understanding these basic commands provides a foundation for more advanced Linux administration and cybersecurity tasks.
<img width="1600" height="900" alt="file-management-practice" src="https://github.com/user-attachments/assets/0883114d-b303-4905-b4ba-ebb86b14284c" />

