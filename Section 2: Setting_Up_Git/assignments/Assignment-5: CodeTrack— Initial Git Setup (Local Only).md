# Assignment 5: CodeTrack – Initial Git Setup (Local Only)

## Objective
Before contributing to the **CodeTrack project** at **CloudAdvisory**, you need to set up Git correctly on your local system.  
This assignment will help you apply what you learned in the **Configuring Git lecture** by setting up your Git **username and email** both **globally** and **locally**.

---

## Prerequisites
- **Git installed** (Git Bash on Windows, Terminal on macOS/Linux)  
- Basic terminal navigation skills  

---

## Task 1 — Create a Local Project Directory

We’ll simulate creating a new CodeTrack project for development.  

### Windows (Command Prompt or PowerShell):
```powershell
mkdir CodeTrack
cd CodeTrack
````

### macOS/Linux (Terminal):

```bash
mkdir CodeTrack && cd CodeTrack
```

### Initialize Git:

```bash
git init
```

**Expected Output:**

```
Initialized empty Git repository in .../CodeTrack/.git/
```

(Optional check for hidden `.git` folder):

```bash
ls -a      # macOS/Linux
dir /a     # Windows
```

**Note:** Take a screenshot of `git init` output for submission.

---

## Task 2 — Configure Git Locally for CodeTrack

Configure Git identity **only for this repository**.
(This is recommended in team/enterprise scenarios when identities differ by project.)

```bash
git config --local user.name "Your Name"
git config --local user.email "your.email@example.com"
git config --local --list
```

**Expected Output:**

```
user.name=Your Name
user.email=your.email@example.com
```

**Tip:** If you’ll push to GitHub and want to keep your email private, use GitHub’s noreply email:

```
12345678+username@users.noreply.github.com
```

**Note:** Take a screenshot of `git config --local --list` output for submission.

---

## Task 3 — Configure Git Globally (Optional, Recommended)

Set your **default Git identity** for all repositories on this machine.

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
git config --global --list
```

**Expected Output:**

```
user.name=Your Name
user.email=your.email@example.com
```

### When to use which?

* **Global:** Use for your standard identity across personal projects.
* **Local:** Use to override per project (e.g., work vs personal).

**Note:** Take a screenshot of `git config --global --list` output for submission.

---

## How to Submit Your Assignment

### For Live Cohort Students

Please follow the submission guidelines explained during the live session.

DevOps Micro Internship [Assignment Master Sheets](https://docs.google.com/spreadsheets/d/1HnlenHEjytvLJMy84bBF-5B1RABaY_BjbfwCj-qnvHM/edit?gid=1951781267#gid=1951781267)

### For Self-Paced Udemy Students

Submit the assignment by clicking **“Next”** and answering the provided questions.
