# **Viewing Commit History in Git**

As we work on a project, we make multiple commits to track changes in our code. Over time, these commits form a **history** of the project, allowing us to see who made changes, what was changed, and when.

To view this **commit history**, we use the `git log` command.

### **Why is commit history important?**
- It helps **track all changes** made to the project **over time**.  
- It provides a **reference** for **debugging issues**.  
- It allows collaboration by showing **who made specific changes**.  
- It gives us a way to **roll back** to a previous commit if needed.

---

## **What is `git log`?**
`git log` is a command that **displays the commit history** in a Git repository. It lists all commits in **reverse chronological order** (newest commits first).

Each commit in the log shows:
- **Commit Hash** – A unique identifier for each commit.
- **Author** – The person who made the commit.
- **Date & Time** – When the commit was made.
- **Commit Message** – A description of what changes were made.

**Analogy:** Think of `git log` as a **diary** that keeps track of all the updates made to your project.

---

## **Using `git log`**
### **Step 1: Viewing Commit History**
To see a list of all commits in your repository, use:
```
git log
```
**Expected Output**:
```
commit 4f5a6b7c8d9e (HEAD -> master)
Author: John Doe <johndoe@example.com>
Date:   Mon Feb 19 10:00:00 2025 +0000

    Modified index.html file and added style.css

commit 1a2b3c4d5e6f
Author: John Doe <johndoe@example.com>
Date:   Sun Feb 18 15:30:00 2025 +0000

    Initial commit
```
This shows:
- The most recent commit **at the top**.
- **Commit hash** (`4f5a6b7c8d9e`) – a unique ID for the commit.
- **Author name & email**.
- **Date & time** of the commit.
- **Commit message** describing the change.

---

## **Making Changes & Viewing Commit History**
Let’s go through an example where we modify a file, commit the changes, and then check the commit history.

### **Step 1: Modify a File**
Modify an existing file (e.g., `index.html`) using an editor.
```
vim index.html
```
After making changes, save and exit.

### **Step 2: Check Repository Status**
Run `git status` to check the status of the repository:
```
git status
```
**Expected Output**:
```
Modified: index.html
```
This shows that `index.html` has been modified but not yet staged.

### **Step 3: Add Changes to Staging Area**
Before committing, stage the changes:
```
git add .
```
This adds **all modified files** to the **staging area**.

### **Step 4: Commit the Changes**
Now, commit the changes with a descriptive message:
```
git commit -m "Updated index.html content"
```
**Expected Output**:
```
[master 2b3c4d5] Updated index.html content
 1 file changed, 5 insertions(+), 2 deletions(-)
```

### **Step 5: Check Commit History Again**
Run `git log` to view the updated commit history:
```
git log
```
**Expected Output**:
```
commit 2b3c4d5e6f7g (HEAD -> master)
Author: John Doe <johndoe@example.com>
Date:   Mon Feb 19 10:30:00 2025 +0000

    Updated index.html content

commit 4f5a6b7c8d9e
Author: John Doe <johndoe@example.com>
Date:   Mon Feb 19 10:00:00 2025 +0000

    Modified index.html file and added style.css

commit 1a2b3c4d5e6f
Author: John Doe <johndoe@example.com>
Date:   Sun Feb 18 15:30:00 2025 +0000

    Initial commit
```
---

## **Commit Hash: Why is it Important?**
Each commit has a **unique commit hash**, such as:
```
commit 2b3c4d5e6f7g
```
The commit hash helps us:
- **Identify** a specific commit.
- **Revert** to an older commit if needed.
- **Compare** changes between commits.

---

## **Simplifying Commit History**
The default `git log` output is **detailed**. You can simplify it using:
```
git log --oneline
```
**Example Output**:
```
2b3c4d5 Updated index.html content
4f5a6b7 Modified index.html file and added style.css
1a2b3c4 Initial commit
```
This shows only:
- The commit hash (shortened).
- The commit message.

---

## **Key Takeaways**
✔️ `git log` shows a detailed history of commits in a Git repository.  
✔️ Each commit has a **unique hash**, **author name**, **timestamp**, and **commit message**.  
✔️ The `git log --oneline` command provides a **simplified view**.  
✔️ Keeping clear commit messages helps in tracking project changes efficiently.  

In the next lecture, we will explore **Git Branching**, which allows developers to work on multiple versions of a project simultaneously. 🚀
