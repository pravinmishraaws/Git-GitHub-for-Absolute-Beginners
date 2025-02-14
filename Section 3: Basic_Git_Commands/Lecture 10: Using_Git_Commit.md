# **Study Notes: Using Git Commit**

Now that we understand how to add files to the **staging area** using `git add`, it’s time to learn how to **save** our changes permanently in the Git repository using `git commit`.

When we modify a file, Git **does not automatically save those changes**. Instead, we need to **commit** our work to track changes properly. This helps keep a clear history of what was changed, when, and why.

Think of **Git commits** as **checkpoints in your project**—they help you go back in time if needed and provide a structured way to track project changes.

---

## **What is `git commit`?**
The `git commit` command **permanently records** changes from the **staging area** into the **repository**.

✅ It **saves your work** in Git’s version history.  
✅ It assigns a **unique identifier** (commit hash) to each change.  
✅ It allows you to **roll back changes** if needed.  
✅ It helps **collaborators** understand what changes were made.

💡 **Analogy:** Think of **committing** like submitting an assignment in school. Until you submit it, your teacher (Git) doesn't recognize your progress.

---

## **Understanding Commit Messages**
Every commit includes a **message** that explains what changes were made.  

This message is important because:
- It helps developers **understand the purpose of the commit**.
- It allows teams to **collaborate efficiently**.
- It serves as a **historical reference** for future debugging.

### **Commit Message Format**
When committing changes, we use the `-m` flag to provide a short description of the commit:
```
git commit -m "Short message describing the change"
```

✅ **Good commit message examples**:
```
git commit -m "Fixed navigation bar responsiveness"
git commit -m "Updated README with project setup instructions"
git commit -m "Refactored API response handling"
```

🚫 **Bad commit message examples**:
```
git commit -m "Fixed stuff"
git commit -m "Updated files"
git commit -m "Commit changes"
```
A **clear and meaningful** commit message improves collaboration and code maintenance.

---

## **How to Commit Changes**
### **Step 1: Ensure Changes are Staged**
Before committing, make sure your files are added to the **staging area** using:
```
git add .
```

### **Step 2: Commit the Changes**
Once your files are staged, commit them using:
```
git commit -m "Initial commit"
```
✅ **Expected Output**:
```
[master (root-commit) 1a2b3c4] Initial commit
 1 file changed, 10 insertions(+)
 create mode 100644 index.html
```
This means:
- Git has successfully **recorded** your changes.
- **1 file changed** (index.html).
- **10 lines** were added.
- A unique **commit hash** (`1a2b3c4`) was generated.

---

## **Viewing Commit History**
After making commits, you can view the commit history using:
```
git log
```
This shows:
- **Commit hash** (unique identifier)
- **Author of the commit**
- **Date and time**
- **Commit message**

✅ **Example Output**:
```
commit 4f5a6b7c8d9e (HEAD -> master)
Author: John Doe <johndoe@example.com>
Date:   Mon Feb 19 10:00:00 2025 +0000

    Initial commit
```

---

## **Key Takeaways**
✔️ `git commit` saves changes **permanently** in Git’s history.  
✔️ Every commit requires a **descriptive message** to explain what changed.  
✔️ Commit history can be viewed using `git log`.  
✔️ A commit is like a **snapshot of your project** at a specific point in time.  

Now that we have committed our changes, let’s move on to **viewing commit history** in the next lecture. 🚀
