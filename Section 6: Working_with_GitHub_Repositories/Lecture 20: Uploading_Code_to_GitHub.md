# **Study Notes: Uploading Code to GitHub**

Now that we have successfully **linked our local repository** to GitHub, the next step is to **upload our code** from the local repository to the remote repository. 

Even though our local repository is linked, **GitHub does not automatically receive our files**. We must **push** them manually using the **`git push`** command.

In this lesson, we will:
- Learn **what `git push` does**.
- Upload our code to **GitHub**.
- Verify that our files are successfully pushed.
- Understand how `git pull` helps us sync changes from **GitHub** to our local repository.

---

## **What is `git push`?**
### **Uploading Local Changes to GitHub**
The **`git push`** command is used to send the changes from your **local repository** to the **remote repository** on GitHub.

### **Why Do We Need `git push`?**
- Your local repository is a **separate copy** of the project.
- Git **does not automatically** upload changes when you edit files locally.
- You must explicitly **push** your changes to make them available on **GitHub**.

### **How `git push` Works**
✅ It **uploads new files** from the local repository to the remote repository.  
✅ It **updates existing files** on GitHub with the latest changes from your local repository.  
✅ It makes sure that the remote repository is **up-to-date** with the latest local changes.  

Think of **`git push`** like uploading a **document** to Google Drive. Once uploaded, your team can access the latest version.

---

## **Step 1: Making Changes in the Local Repository**
Before pushing, let’s ensure we have changes to upload:

1️⃣ **Open the terminal (Git Bash/Command Prompt).**  
2️⃣ Navigate to your **local Git repository**:
   ```
   cd path/to/your-repository
   ```
   Example:
   ```
   cd ~/Documents/Mini-Finance
   ```
3️⃣ **Create a new file or modify an existing file.**  
   Example (creating a new file):
   ```
   touch about.html
   ```
   Example (modifying an existing file):
   ```
   echo "<!-- Updated About Page -->" >> about.html
   ```

4️⃣ **Check the status of your repository:**
   ```
   git status
   ```
   This will show **untracked files** or files with **changes**.

---

## **Step 2: Staging and Committing Changes**
Before pushing, we need to **stage** and **commit** our changes:

1️⃣ **Stage all changes:**  
   ```
   git add .
   ```
2️⃣ **Commit changes with a message:**  
   ```
   git commit -m "Added About page"
   ```

At this point, our changes are recorded **locally** but **not yet uploaded to GitHub**.

---

## **Step 3: Pushing Code to GitHub**
Now that our changes are committed, let’s upload them to **GitHub**.

1️⃣ Use the **`git push`** command:
   ```
   git push origin master
   ```
   - `origin` → This is the **remote repository** (GitHub).
   - `master` → This is the **branch** we are pushing to.

✅ **Expected Output:**
```
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Writing objects: 100% (5/5), 543 bytes | 543.00 KiB/s, done.
Total 5 (delta 0), reused 0 (delta 0)
To https://github.com/yourusername/Mini-Finance.git
```

---

## **Step 4: Verifying the Uploaded Code**
To confirm our code is successfully pushed:

1️⃣ **Go to GitHub** and open your repository.  
2️⃣ **Refresh the page**.  
3️⃣ You should see the **new files** or **updated files** appear in the repository.

Congratulations! 🎉 Your local code is now **live on GitHub**.

---

## **What is `git pull`?**
Just like `git push` **uploads changes**, `git pull` **downloads changes**.

Let’s say a teammate makes modifications to the **GitHub repository**. You need to **update your local repository** with their changes.

### **Using `git pull`**
To **sync your local repository** with GitHub:
```
git pull origin master
```
- **`git pull`** downloads the latest changes.
- **It merges** them with your local repository.
- If there are conflicts, **Git will ask you to resolve them**.

---

## **Understanding `git push` vs `git pull`**
| Command       | Purpose |
|--------------|---------|
| `git push`   | Uploads local changes to GitHub. |
| `git pull`   | Downloads and merges changes from GitHub to your local machine. |

---

## **Summary: Key Takeaways**
- **`git push`** is used to upload code from your local repository to GitHub.
- Before pushing, you must **stage (`git add`)** and **commit (`git commit`)** changes.
- **After pushing**, the changes will appear in the remote repository on GitHub.
- **`git pull`** is used to fetch and merge the latest changes from GitHub to your local repository.
- Keeping your local and remote repositories in sync is essential for **team collaboration**.

---

## **What’s Next?**
Now that we have successfully **pushed our code to GitHub**, let’s move on to another essential GitHub feature—**cloning a repository**.

In the next lesson, we will learn **how to clone a remote GitHub repository** onto our local machine, so we can start working on an existing project.

**Let’s continue learning!**
