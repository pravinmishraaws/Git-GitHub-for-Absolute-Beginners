### **Study Notes: Merging Branches with Git Merge**  

NOw, let's understand **Why Do We Need Git Merge?**  

So far, we have learned how to **create branches** and **switch between them** using `git checkout`. But in a real-world project, developers don’t just work in separate branches forever—they **merge** their work back into the main branch.  

Let’s say you're working on a **website project** with a team:  
- One developer is working on the **homepage** in `homepage-branch`.  
- Another is working on the **about us page** in `aboutus-branch`.  
- Once both sections are completed, you need to **combine them** back into the main website.  

This is exactly what **Git Merge** does! It **combines changes** from one branch into another, ensuring that all updates are incorporated into the main codebase.  

---

## **Understanding Git Merge**  

The `git merge` command allows you to:  
✔️ **Combine changes** from different branches into one.  
✔️ **Keep a clean and structured workflow** when working in teams.  
✔️ **Integrate new features or bug fixes** without disrupting the main code.  

Think of `git merge` like merging two documents:  
- You have a **main document (master branch)**.  
- A colleague works on a **copy (feature branch)** and makes improvements.  
- You **merge** the improved copy back into the main document.  

---

## **Steps to Merge a Branch into Master**  

### **Step 1: Ensure Your Repository is Up-to-Date**  

Before merging, always make sure you are on the **main branch**. Run:  

```sh
git checkout master
```

✅ **Expected Output:**  
```
Switched to branch 'master'
```

### **Step 2: Merge a Branch into Master**  

To merge another branch (e.g., `develop`) into `master`, use:  

```sh
git merge develop
```

✅ **Expected Output:**  
```
Updating 3f5b2d6..7c9a5f2
Fast-forward
 style.css | 10 +++++++++-
 1 file changed, 10 insertions(+), 1 deletion(-)
```

This means the changes from `develop` have been successfully **merged into `master`**! 🎉  

### **Step 3: Verify the Merge**  

Check if the changes are now in `master`:  

```sh
cat style.css
```

If you see the **updates from the `develop` branch**, the merge was successful!  

---

## **Handling Merge Conflicts**  

### **What is a Merge Conflict?**  

Sometimes, two people make changes to the same section of a file in different branches. When merging, Git doesn’t know **which change to keep**, so it asks **you** to decide.  

### **How to Resolve Merge Conflicts**  

1️⃣ Run `git merge <branch-name>` → Git will **detect conflicts** and stop merging.  

2️⃣ Open the conflicting file in an editor (e.g., `style.css`). You’ll see something like this:  

```css
<<<<<<< HEAD
background-color: blue;
=======
background-color: red;
>>>>>>> develop
```

3️⃣ **Manually edit the file** and decide which version to keep. For example:  

```css
background-color: blue;
```

4️⃣ **Stage and commit the resolved file**:  

```sh
git add style.css
git commit -m "Resolved merge conflict in style.css"
```

Now the merge is complete!  

---

## **Key Takeaways**  

-  `git merge <branch-name>` → **Merge changes from one branch into another**  
-  `git checkout master` → **Switch to the master branch before merging**  
-  **Fast-Forward Merge** → When there are no conflicts, changes are merged directly  
-  **Merge Conflicts** → When changes overlap, Git asks for manual resolution  

---

## **What’s Next?**  

Now that we’ve learned how to **merge changes**, we are ready to **push our project to GitHub**!  

In the next section, we will explore how to:  
- Upload our local repository to GitHub.  
- Pull changes from a remote repository.  

Let’s take our project to the next level! 🚀
