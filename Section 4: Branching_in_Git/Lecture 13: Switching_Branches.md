### **Study Notes: Switching Branches with Git Checkout**  

Now, let's understand **Why Do We Need to Switch Branches?**  

In the previous lecture, we learned how to **create a new branch**. But creating a branch alone isn’t enough—we need to **switch to it** before we can start working.  

Imagine you’re working on a **website project**.  

- The **master branch** contains the stable, working version of the site.  
- You create a new branch called `develop` to add a new feature.  
- To start making changes, you **must switch from `master` to `develop`**.  

This is where the **`git checkout`** command comes in!  

---
## **What is `git checkout`?**  

`git checkout` allows you to:  
- **Switch between different branches** in your project.  
- **Revert to a previous commit or version** of your code.  
- **Navigate between different stages** of your project history.  

---
## **How to Switch Branches Using Git Checkout**  

### **Step 1: View All Available Branches**  
Before switching, let’s check which branches exist in our repository.  

```sh
git branch
```

✅ **Expected Output:**  
```
  develop
* master
```
Here, the `*` symbol indicates that you are currently on the **master branch**.  

### **Step 2: Switch to Another Branch**  

To switch to a different branch (e.g., `develop`), use:  

```sh
git checkout develop
```

✅ **Expected Output:**  
```
Switched to branch 'develop'
```
Now, all changes you make will be in the `develop` branch, **without affecting the master branch**.  

---
## **Making Changes in a New Branch**  

Once we switch to the `develop` branch, we can start **modifying files**.  

### **Example: Editing a CSS File in `develop` Branch**  

1️⃣ Open the `style.css` file using an editor:  

```sh
vi style.css
```
2️⃣ Modify the styles, then **save the changes**.  

3️⃣ **Stage and commit** the changes:  

```sh
git add style.css
git commit -m "Modified style.css from the develop branch"
```

---
## **Verifying That Changes Stay in the New Branch**  

Now, let’s **switch back** to the `master` branch:  

```sh
git checkout master
```

If you check the `style.css` file in the `master` branch, you’ll notice that **the changes you made in `develop` are NOT present in `master`**.  

✅ This proves that **each branch maintains its own version of the code!**  

---
## **Reverting to a Previous Commit Using `git checkout`**  

Imagine you made some changes but realize they were a mistake. You want to **go back to an earlier version** of your project.  

### **Step 1: Find the Commit Hash**  

1️⃣ Use `git log` to view commit history:  

```sh
git log
```

✅ **Example Output:**  
```
commit 3f5b2d6f4d6a7d (HEAD -> develop)
Author: Your Name
Date: Mon Feb 12 12:34:56 2025 +0000

    Modified style.css

commit d4f7a6b8c8d9e (master)
Author: Your Name
Date: Mon Feb 10 15:20:00 2025 +0000

    Initial commit
```
2️⃣ Copy the **commit hash** of the version you want to go back to (e.g., `d4f7a6b8c8d9e`).  

### **Step 2: Checkout the Previous Version**  

```sh
git checkout d4f7a6b8c8d9e
```

✅ **Expected Output:**  
```
Note: switching to 'd4f7a6b8c8d9e'.
```
Now, your project files are restored to that **older version**!  

---
## **Returning to the Latest Version**  

After checking an old commit, you may notice that you are now in a **detached HEAD state** (meaning you’re viewing an old version but not actively on a branch).  

To return to the latest commit in the `master` branch, run:  

```sh
git checkout master
```

✅ **Expected Output:**  
```
Switched to branch 'master'
```
Now you’re back to the latest version!  

---
## **Key Takeaways**  

✔️ `git checkout <branch-name>` → **Switch between branches**  
✔️ `git checkout <commit-hash>` → **Revert to an older commit**  
✔️ `git log` → **Find commit history**  
✔️ Switching branches keeps changes **isolated**, preventing accidental modifications in the main branch  

---
## **What’s Next?**  

Now that we know how to switch branches, the next step is learning how to **merge changes from one branch into another**.  

In the next lesson, we’ll cover **Git Merge**—how to combine changes safely! 🚀
