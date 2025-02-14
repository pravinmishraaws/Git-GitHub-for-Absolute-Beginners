### **Study Notes: Introduction to Git Branches**  

Well, now let's start with: **Why Do We Need Git Branching?**  

Imagine you’re working on a **website project** with a team. You’ve been assigned a **new feature** to add, but you don’t want to accidentally break the existing code.  

How can you **safely** work on this feature **without affecting** the main website?  

This is where **Git branches** come in!  

A **branch** in Git allows developers to **work on different versions of the same project** simultaneously, without interfering with each other's work.  

---
## **What is a Git Branch?**  

A **branch** is a **separate version** of your project where you can make changes **independently** without affecting the main project.  

By default, when we create a Git repository, Git automatically creates a **default branch** called **master** (or **main** in newer versions).  

**Think of it like this:**  
- The **master branch** is your **main project**—the stable, working version of your code.  
- When you create a **new branch**, you get an **exact copy** of the master branch.  
- You can now work on **new features** in this branch **without touching** the master code.  

---
## **Real-World Example: Working with Branches**  

Let’s say you are **building a website** with your team.  

- You are asked to **add a new "Profile" page**.  
- Instead of editing the main code directly, you create a **new branch** called `profile-page`.  
- You make all your **changes safely** in this branch.  
- Once everything is **working correctly**, you merge the changes **back into the master branch**.  

**While you are working on `profile-page`, your teammates can continue working on the `master` branch without any conflicts!**  

---
## **Creating a Branch in Git**  

To create a new branch, we use the **`git branch`** command:  

```sh
git branch develop
```

**This command creates a new branch named `develop` but does NOT switch to it yet.**  

To check if the branch was created, list all branches using:  

```sh
git branch
```

**Expected Output:**  
```
  develop
* master
```

Here, the `*` symbol indicates which branch you are currently on (default: `master`).  

---
## **Visualizing Git Branches**  

**Think of Git branches like a tree:**  

- The **trunk** of the tree is the **master branch**—this is where your stable, working code lives.  
- Each **branch** represents a new feature, bug fix, or experiment.  
- You can **create branches, modify them, and merge them back** when ready.  

```
    master
       │
       ├─── develop  (New branch)
       ├─── profile-page  (Another branch)
```

---
## **Why Use Git Branching?**  

✔️ **Work on multiple features at the same time** without affecting the main project.  
✔️ **Fix bugs independently** without disrupting development.  
✔️ **Test new ideas safely** without modifying the master branch.  
✔️ **Collaborate easily**—each developer can work on their own branch.  

---
## **What’s Next?**  

Now that we have created a branch, we need to **switch between branches** to start working on them.  

In the next lesson, we’ll learn how to **switch branches** using `git checkout` and `git switch`.
