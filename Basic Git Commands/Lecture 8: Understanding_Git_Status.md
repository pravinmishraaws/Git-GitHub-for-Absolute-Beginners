### **Study Notes: Understanding `git status`**  

Now that we have successfully initialized our Git repository and created our first file, it’s time to **check the status of our repository** using the `git status` command.  

But before we begin, let's ask ourselves:  

- **How do we know which files Git is tracking?**  
- **How can we check if our changes have been saved or not?**  

Now, I will help us understand how Git organizes and tracks changes in our files.

---

## **1️⃣ What is `git status`?**  
The `git status` command gives us **a snapshot of our Git repository** at any given moment. It tells us:  

✔ **Which files are untracked** (new files that Git hasn’t started tracking yet)  
✔ **Which files have been modified** (files that were changed but not yet saved to Git)  
✔ **Which files are ready to be committed** (files that are staged and waiting to be saved)  

Think of `git status` as **a checklist**—it ensures that you don’t forget to save important changes before moving forward.

---

## **2️⃣ Checking the Status of Our Git Repository**
Let’s go step by step and see `git status` in action.

### **Step 1: Open Git Bash and Navigate to Your Repository**
First, make sure you're inside your Git repository. If not, navigate to it using:

```bash
cd Mini-Finance
```

Then, confirm your current location:

```bash
pwd
```

This should display the path of your **Mini-Finance** project folder.

---

### **Step 2: Run `git status`**
To check the current state of our repository, type:

```bash
git status
```

If you just initialized the repository and haven't added any files yet, you will see an output like:

```
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        index.html
```

---

## **3️⃣ Understanding the Output**
Let’s break down the key parts of this message.

- **"On branch master"** – This tells us which branch we are on (we will cover branches later).  
- **"No commits yet"** – This means we haven't saved any changes in Git yet.  
- **"Untracked files:"** – This section lists files that **exist in our folder but are not being tracked by Git** yet.  

In our case, `index.html` is listed as an **untracked file**.

---

## **4️⃣ What Does "Untracked File" Mean?**
An **untracked file** is a file that exists in our Git repository but is **not yet being tracked**.  

💡 **Think of an untracked file like a draft on your computer**—you’ve written it, but it hasn’t been officially saved anywhere yet.

For Git to start tracking the file, we need to **add it to the staging area** (we will cover this in the next lecture).

---

## **5️⃣ The Importance of `git status`**
When working on a project, we may:
- **Create new files**
- **Modify existing files**
- **Forget to save some changes**

By running `git status`, we can always check:
✔ **What files have been added but not tracked yet**  
✔ **What files have been modified since the last save**  
✔ **Which files are ready to be committed**  

It acts as a **checkpoint** before we move forward.

---

## **📝 Summary**
✔ **We learned about `git status` and its role in Git.**  
✔ **We ran `git status` to check the status of our repository.**  
✔ **We understood what "untracked files" mean in Git.**  

---

## **🚀 What’s Next?**
Right now, our `index.html` file **exists but is not tracked**.  
In the next lesson, we will **add files to Git using `git add`** and prepare them for the Staging!
