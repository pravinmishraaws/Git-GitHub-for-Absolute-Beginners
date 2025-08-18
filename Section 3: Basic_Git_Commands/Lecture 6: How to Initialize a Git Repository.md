# Lab – How to Initialize a Git Repository

## 1. Why Initialize a Repository?

* A **normal folder** can store files but cannot track changes.
* To track versions, we must **convert the folder into a Git repository**.
* Git does this by creating a hidden **`.git` folder**, which stores all history & configuration.

---

## 2. Step-by-Step Commands

### Step 1: Check Current Directory

```bash
pwd
```

* Shows the **present working directory** (where you are on your system).

---

### Step 2: Create a New Folder

```bash
mkdir project
ls
```

* `mkdir project` → creates a folder named `project`.
* `ls` → lists files/folders in the current directory.

---

### Step 3: Navigate into the Folder

```bash
cd project
```

* `cd` → change directory into the `project` folder.

---

### Step 4: Create Another Folder Inside

```bash
mkdir the-cloud-advisory
cd the-cloud-advisory
```

* Creates a subfolder `the-cloud-advisory` → we’ll turn this into a Git repository.

---

### Step 5: Initialize Git Repository

```bash
git init
```

* Converts the current folder into a **Git repository**.
* Git creates a hidden `.git` folder → contains all version control info.

---

### Step 6: Verify Hidden `.git` Folder

```bash
ls -a
```

* `-a` shows hidden files.
* You should see `.git` → confirms the folder is now a Git repo.

---

## 3. What Happened Behind the Scenes?

* **Before `git init`** → folder was just a normal directory.
* **After `git init`** → folder became a **Git repository** with:

  * `.git` folder (stores commits, branches, logs, etc.).
  * Ability to track file changes.

---

## 4. Next Steps

* Now that the repo is initialized, you can use other Git commands:

  * `git status` → check repo status.
  * `git add` → stage files.
  * `git commit` → save changes.
  * `git push` → send changes to a remote repo.

---

### Key Takeaway:
✅  Running `git init` transforms a simple folder into a **Git repository** by adding the hidden `.git` folder. This is the foundation for tracking and managing your project with Git.

