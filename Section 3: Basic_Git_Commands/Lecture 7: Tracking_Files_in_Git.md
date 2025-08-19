### Creating and Tracking Files in Git**  
Now that we have successfully initialized our Git repository, it’s time to take the next step—**creating files and tracking changes!**  

---

## **1️⃣ Creating a File Inside the Git Repository**  
A Git repository without files is like an **empty notebook**—it’s ready to store information, but there's nothing written in it yet.  

Let’s create our first file inside our Git repository.  

### **Step 1: Open Git Bash (or Terminal)**
Make sure you are inside your Git repository. If not, navigate to it using:  

```bash
cd Mini-Finance
```

You can confirm you are inside the right directory by running:

```bash
pwd
```
This should show the correct path to your **Mini-Finance** folder.

---

### **Step 2: Create a New File**
To create a new file, we use the `touch` command followed by the file name.  

Let's create an **index.html** file:  

```bash
touch index.html
```

- This command **creates an empty file** named `index.html`.  
- You can verify the file was created by listing all files using:

```bash
ls
```

If successful, you should see **index.html** in the output.

---

## **2️⃣ Writing Code Inside the File**  
Now that we have our `index.html` file, let’s add some content to it.

### **Option 1: Using a Code Editor**
You can open `index.html` in any text editor such as:
- **VS Code:** `code index.html`
- **Nano (for Linux/Mac):** `nano index.html`

### **Option 2: Using the Terminal (VI Editor)**
If you're comfortable with command-line editors, you can use `vi`:

```bash
vi index.html
```

This will open the file in the **VI editor**.  
Now, press `i` to enter insert mode and add the following code:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mini Finance</title>
</head>
<body>
    <h1>Welcome to Mini Finance</h1>
    <p>This is a basic HTML file created inside a Git repository.</p>
</body>
</html>
```

Once done, press `ESC`, then type `:wq` and hit `Enter` to **save and exit**.

**Congratulations!** You just created and edited your first file inside Git.  

---

## **3️⃣ Checking if Git is Tracking the File**
Since our file is inside a Git repository, Git should **recognize** it, right? Let’s check.

Run the following command:

```bash
git status
```

This command **shows the current state of your repository**.  
You should see something like this:

```
Untracked files:
  (use "git add <file>..." to include in what will be committed)

        index.html
```

### **What Does This Mean?**
- The `index.html` file is **not being tracked yet**.
- Git knows the file **exists** but is waiting for us to tell it what to do next.

---

## ** Summary**
✔ **We created a new file** (`index.html`) inside our Git repository.  
✔ **We added content** to the file using an editor.  
✔ **We checked the file status** using `git status`, which showed that Git is aware of the new file but is not tracking it yet.  

---

## **🚀 What’s Next?**
Git can now see our file, but it **isn't tracking it yet**. In the next lesson, we will learn in details about **git status**!
