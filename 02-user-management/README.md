# 02 — User Management

This section covers basic Linux commands used to identify users, view user information, create and manage user accounts, and check user activity.

These commands are fundamental for Linux system administration and are particularly important in cybersecurity because user accounts and permissions determine who can access and interact with a system.

## Commands Covered

### 1. `whoami` — Display Current User

Displays the username of the currently logged-in user.

```bash
whoami
```

**Example:**

```bash
whoami
```

**Use case:**
Useful for confirming which user account is currently being used.

---

### 2. `id` — Display User Information

Displays the user ID (UID), group ID (GID), and groups associated with a user.

```bash
id
```

**Example:**

```bash
id
```

You can also check another user:

```bash
id username
```

**Use case:**
Useful for checking user identities, group memberships, and privileges.

---

### 3. `who` — Display Logged-in Users

Shows the users currently logged into the system.

```bash
who
```

**Example:**

```bash
who
```

**Use case:**
Useful for checking who currently has an active session on a Linux system.

---

### 4. `w` — Display User Activity

Shows logged-in users and information about what they are currently doing.

```bash
w
```

**Example:**

```bash
w
```

**Use case:**
Useful for monitoring active user sessions and investigating unexpected activity.

---

### 5. `users` — List Logged-in Users

Displays the usernames of users currently logged into the system.

```bash
users
```

**Example:**

```bash
users
```

**Use case:**
Provides a quick way to see which users currently have active sessions.

---

### 6. `sudo` — Execute Commands as Administrator

Allows an authorized user to execute commands with elevated privileges.

```bash
sudo command
```

**Example:**

```bash
sudo apt update
```

**Use case:**
Useful for performing administrative tasks that require elevated privileges.

**Security note:**
Administrative privileges should be used carefully because excessive privileges can increase the impact of a compromised account.

---

### 7. `adduser` — Create a User

Creates a new user account.

```bash
sudo adduser username
```

**Example:**

```bash
sudo adduser labuser
```

**Use case:**
Useful for creating separate accounts for users on a Linux system.

---

### 8. `passwd` — Change a Password

Changes the password associated with a user account.

```bash
sudo passwd username
```

**Example:**

```bash
sudo passwd labuser
```

**Use case:**
Useful for setting or changing user passwords.

---

### 9. `usermod` — Modify a User

Modifies an existing user account.

For example, a user can be added to a group:

```bash
sudo usermod -aG groupname username
```

**Use case:**
Useful for managing user group memberships and access to system resources.

---

### 10. `deluser` — Remove a User

Removes a user account from the system.

```bash
sudo deluser username
```

**Example:**

```bash
sudo deluser labuser
```

**Use case:**
Useful for removing accounts that are no longer required.

---

## Practical Exercise

The following commands were used to practice basic user management:

```bash
whoami
id
who
w
users
sudo adduser labuser
id labuser
sudo passwd labuser
```

This exercise demonstrates how to identify the current user, inspect user information, view active sessions, create a user, and manage a user's password.

## Cybersecurity Relevance

User management is an important part of Linux security.

Security professionals may need to:

* Identify users currently accessing a system.
* Investigate unexpected user activity.
* Check user IDs and group memberships.
* Create and remove user accounts.
* Manage administrative privileges.
* Control access to system resources.

Understanding user management provides a foundation for learning about Linux permissions, privilege escalation, and access control.

## Key Takeaway

Understanding Linux users is essential for managing system access and maintaining security. User accounts, groups, and privileges determine what users can access and what actions they can perform.

