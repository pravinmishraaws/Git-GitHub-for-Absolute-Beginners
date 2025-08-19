### **Using `git add` to Stage Changes**  

Now that we have created and modified a file inside our Git repository, we need a way to **prepare it for saving**. Git doesn’t automatically track every change we make—instead, we need to **manually tell Git which changes should be included in the next save** (also known as a commit).  

This is where `git add` comes in!  

**Think of `git add` as preparing a package for shipment.**  
- Imagine you are packing a box for delivery.  
- You gather all the items you want to send and put them in the box.  
- But until you seal the box and ship it, those items haven’t officially left your home!  

Similarly, `git add` is like putting changes inside a **box** (staging area), but they are not permanently saved yet. **The next step (commit) will officially store them in Git.**  

---

## **2️⃣ What is the Git Staging Area?**  

The **staging area** is an **intermediate step** between making changes and saving them permanently in Git. It acts as a buffer where we **review and organize** changes before making them official.  

Here’s how it works:  
1. **Modify a file** – You change a file in your project.  
2. **Run `git add`** – The file is added to the **staging area** (prepared for commit).  
3. **Run `git commit`** – The file is **permanently saved** in Git’s version history.  

**Key Point:**  
Git will **not track your changes** unless they are added to the **staging area** using `git add`.  

---

## **3️⃣ Checking File Status Before Using `git add`**  

Before adding our file, let’s check its current status in the repository. Open **Git Bash (or Terminal)** and navigate to your project folder:

```bash
cd Mini-Finance
```

Now, check the repository status:

```bash
git status
```

Expected Output:
```
On branch master

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        index.html
```

This tells us that `index.html` **exists but is not tracked by Git** yet.

---

## **4️⃣ Adding Files to the Staging Area with `git add`**  

To tell Git that we want to start tracking `index.html`, we **add it to the staging area** using:  

```bash
git add index.html
```

Let’s check the status again:

```bash
git status
```

Expected Output:
```
On branch master

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

        new file:   index.html
```

Now, `index.html` is **in the staging area** and ready to be committed!  

**Notice the difference?**  
- Before: The file was **untracked**.  
- After `git add`: The file is now **staged** and **ready for commit**.

---

## **5️⃣ Staging Multiple Files at Once**  

Instead of adding files one by one, we can add **all modified files** at once using:  

```bash
git add .
```

This will add **all new and modified files** inside the repository to the staging area.

---

## **6️⃣ Summary**  

**`git add` moves changes to the staging area, preparing them for commit.**  
**The staging area is like a shipping box—it collects changes before they are officially saved.**  
**We use `git status` to check which files are staged and ready for commit.**  
**We can add one file at a time (`git add filename`) or all files at once (`git add .`).**  

---

## **What’s Next?**  

Now that our changes are staged, they still aren’t **permanently saved** in Git.  
In the next lecture, we will **commit our changes** and officially add them to the Git history!
