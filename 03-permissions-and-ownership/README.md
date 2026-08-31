# 03 — Permissions and Ownership

This section covers Linux commands used to view and manage file permissions, ownership, and access to system resources.

Linux permissions are an important part of system security because they control who can read, modify, or execute files and directories.

## Commands Covered

### 1. `ls -l` — View Permissions and Ownership

Displays detailed information about files and directories, including their permissions, owner, group, size, and modification time.

```bash
ls -l
```

**Example:**

```bash
ls -l secret.txt
```

A typical permission entry may look like:

```text
-rw-r--r--
```

The permissions are divided into three sections:

```text
-rw- | r-- | r--
 owner  group  others
```

Where:

* `r` — Read
* `w` — Write
* `x` — Execute

**Use case:**
Useful for checking who owns a file and what permissions have been assigned to it.

---

### 2. `chmod` — Change File Permissions

Changes the permissions of files and directories.

```bash
chmod permissions filename
```

**Example:**

```bash
chmod 600 secret.txt
```

This gives the owner read and write permissions while removing permissions for the group and others.

You can also use symbolic permissions:

```bash
chmod u+x script.sh
```

This gives the file owner permission to execute the script.

**Use case:**
Useful for restricting access to sensitive files and controlling what users can do with files.

---

### 3. `chown` — Change File Ownership

Changes the owner of a file or directory.

```bash
sudo chown username filename
```

**Example:**

```bash
sudo chown labuser secret.txt
```

**Use case:**
Useful for assigning files to the appropriate user and maintaining proper access control.

---

### 4. `chgrp` — Change Group Ownership

Changes the group associated with a file or directory.

```bash
sudo chgrp groupname filename
```

**Example:**

```bash
sudo chgrp users secret.txt
```

**Use case:**
Useful when multiple users need access to files through a shared group.

---

### 5. `stat` — Display Detailed File Information

Displays detailed information about a file or directory.

```bash
stat filename
```

**Example:**

```bash
stat secret.txt
```

The output can include information such as:

* File size
* Permissions
* Owner
* Group
* Access time
* Modification time
* Change time

**Use case:**
Useful during system administration and security investigations when detailed file metadata is required.

---

### 6. `umask` — Control Default File Permissions

Displays or sets the default permission mask used when creating new files and directories.

```bash
umask
```

**Example:**

```bash
umask
```

A common output is:

```text
0022
```

The `umask` helps determine which permissions are removed from the default permissions of newly created files and directories.

**Use case:**
Useful for understanding and controlling the default permissions assigned to newly created files.

---

### 7. `groups` — Display User Groups

Displays the groups that a user belongs to.

```bash
groups
```

**Example:**

```bash
groups
```

You can also check another user:

```bash
groups labuser
```

**Use case:**
Useful for understanding what resources and permissions a user may have access to through group membership.

---

### 8. `getfacl` — View Access Control Lists

Displays detailed access control information for files and directories.

```bash
getfacl filename
```

**Example:**

```bash
getfacl secret.txt
```

Access Control Lists (ACLs) allow permissions to be assigned to specific users or groups beyond the standard owner, group, and others permission model.

**Use case:**
Useful when investigating or managing more detailed access permissions on Linux systems.

---

## Understanding Linux Permissions

Linux permissions are generally represented using three permission categories:

```text
Owner | Group | Others
```

Each category can have three basic permissions:

```text
r = Read
w = Write
x = Execute
```

For example:

```text
-rwxr-xr--
```

This means:

* **Owner:** Read, write, and execute
* **Group:** Read and execute
* **Others:** Read only

Permissions can also be represented using numeric values:

```text
Read    = 4
Write   = 2
Execute = 1
```

For example:

```bash
chmod 600 secret.txt
```

`600` means:

```text
Owner  = 6 → Read + Write
Group  = 0 → No permissions
Others = 0 → No permissions
```

---

## Practical Exercise

The following commands were used to practice Linux permissions and ownership:

```bash
mkdir permission-lab
cd permission-lab
touch secret.txt
ls -l
chmod 600 secret.txt
ls -l
stat secret.txt
getfacl secret.txt
```

This exercise demonstrates how to create a file, inspect its permissions, restrict access, and examine detailed file information.

## Cybersecurity Relevance

Linux permissions and ownership are fundamental to system security.

Security professionals need to understand:

* Who owns files and directories.
* Which users can access sensitive information.
* Which files can be modified or executed.
* How excessive permissions can expose sensitive data.
* How group memberships affect access.
* How incorrect permissions can contribute to security vulnerabilities.

For example, a sensitive file containing credentials should not normally be readable by every user on the system.

Proper permission management follows the principle of **least privilege**, giving users only the access they need.

## Key Takeaway

Linux permissions provide an important layer of access control. Understanding ownership, groups, and permissions makes it possible to control access to files and reduce the risk of unauthorized modification or disclosure of sensitive information.

