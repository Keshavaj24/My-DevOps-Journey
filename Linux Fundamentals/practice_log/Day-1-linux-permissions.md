# Linux Practice Log – Users, Groups & Permissions

## Overview

Today I focused on hands-on Linux practice instead of just watching tutorials.
I practiced managing users, groups, files, and permissions, and debugged real permission errors in a simulated company folder structure.

---

## Skills Practiced

* Creating users and groups
* Assigning users to groups
* Managing directories and files
* Setting file and folder permissions
* Debugging permission issues
* Understanding path traversal

---

## Key Concepts

### File vs Folder Permissions

**Files**

```
r → read file
w → modify/delete file
x → execute file
```

**Folders**

```
r → list files (ls)
w → create/delete files
x → enter folder (cd)
```

---

### Path Traversal Rule

To access a file:

```
/home/user/company-project/dev/app.py
```

User must have **execute (x)** permission on:

```
/
home
user
company-project
dev
```

If any folder blocks access → file cannot be reached.

---

### Users and Groups

Example structure:

```
dev_team     → dev1, dev2
hr_team      → hr1
intern_team  → intern1
```

Commands practiced:

```
whoami
groups
usermod -aG
```

---

### Permission Commands

Commands used:

```
chmod
chown
chgrp
ls -l
ls -ld
```

Examples:

```
chmod 750 folder
chmod 640 file
chown user:group file
```

---

## Practice Project Structure

```
company-project/
├── dev/
│   └── app.py
├── hr/
│   └── employees.txt
└── interns/
    └── notes.txt
```

---

## Permission Design

```
company-project → 751
dev             → 770
hr              → 770
interns         → 750
```

### Result

* Developers access only dev folder
* HR accesses only hr folder
* Interns access only interns folder
* Users cannot access other team folders
* Parent folder allows traversal

---

## Key Takeaways

* Folder permissions behave differently than file permissions
* Groups simplify access control
* Parent directory permissions matter
* Execute (x) allows entering folders
* Read (r) allows listing files
* Write (w) allows modification
* Permissions control access at every directory level

---

## What I Learned

Practicing directly in the terminal helped me understand Linux permissions much better than just watching tutorials. Debugging permission errors made the concepts clear and practical.

---

## Next Steps

* Advanced permissions
* ACLs
* Process management
* Real-world Linux scenarios
