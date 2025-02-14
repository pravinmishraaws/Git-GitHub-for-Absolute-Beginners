# **Configuring Git: Setting Up Your Identity**  

So far, we’ve **installed Git** on our system. But before we start working with repositories, we need to configure Git properly.  

Think of Git as a **collaborative workspace**. Just like when you join a new company, you first introduce yourself, set up your email, and configure your account before you start working on projects, right? Similarly, in Git, **before you start tracking changes or making commits, Git needs to know who you are**.  

## **Why Do We Need Git Configuration?**  

Whenever you **make a change** in a Git-tracked project, Git **records the author** of that change. This is important because:  
- It helps track **who made what change and when**.  
- It allows multiple developers to **work on the same project** without confusion.  
- It helps maintain a **clear history** of contributions.  

For example, let's say you are working on a **team project** in your company. If every change was just labeled as **"Anonymous"**, how would you know **who fixed a bug, who added a new feature, or who made a mistake**? That’s where Git’s configuration comes in!  

---

## **Types of Git Configuration**  

Git allows us to **set up configurations at two levels**:  

### **1️⃣ Local Configuration (Per Repository)**  
- When you configure Git **locally**, it applies only to **a specific project (repository)**.  
- If you switch to another repository, you’ll have to **set up your details again**.  
- This is useful when you work on **multiple projects with different accounts**.  

### **2️⃣ Global Configuration (Applies to All Repositories)**  
- **Global configuration applies to all repositories** on your system.  
- This is useful when you work on multiple repositories **under the same identity**.  
- You **don’t need to configure your details repeatedly** for every project.  

---

## **Setting Up Git Locally (For a Single Repository)**  

To **set your identity** for a **specific repository**, follow these steps:  

### **Step 1: Open Git Bash or Terminal**  
- Navigate to your project folder (your Git repository).  
- If you don’t have a Git repository yet, initialize one using:  
  ```bash
  git init
  ```

### **Step 2: Set Your Name**  
- Use the following command to configure your name:  
  ```bash
  git config --local user.name "Your Name"
  ```
  Example:  
  ```bash
  git config --local user.name "Pravin Mishra"
  ```

### **Step 3: Set Your Email**  
- Similarly, set your email using:  
  ```bash
  git config --local user.email "your-email@example.com"
  ```
  Example:  
  ```bash
  git config --local user.email "hello@pravinmishra.in"
  ```

### **Step 4: Verify Your Configuration**  
- To check whether your name and email have been configured, run:  
  ```bash
  git config --local user.name
  git config --local user.email
  ```
  Expected Output:  
  ```
  Pravin Mishra
  hello@pravinmishra.in
  ```
✔️ If you see your name and email in the output, your Git is now configured **locally** for this repository!  

---

## **Setting Up Git Globally (For All Repositories)**  

If you don’t want to **set up Git for every project separately**, you can configure it **globally**.  

### **Step 1: Open Git Bash or Terminal**  
- You don’t need to be inside a specific repository for global configuration.  

### **Step 2: Set Your Global Name**  
- Run the following command:  
  ```bash
  git config --global user.name "Your Name"
  ```
  Example:  
  ```bash
  git config --global user.name "Pravin Mishra"
  ```

### **Step 3: Set Your Global Email**  
- Similarly, configure your email:  
  ```bash
  git config --global user.email "your-email@example.com"
  ```
  Example:  
  ```bash
  git config --global user.email "hello@pravinmishra.in"
  ```

### **Step 4: Verify Your Global Configuration**  
- Check whether your details were set successfully:  
  ```bash
  git config --global user.name
  git config --global user.email
  ```
  Expected Output:  
  ```
  Pravin Mishra
  hello@pravinmishra.in
  ```

✔️ Now, whenever you create a new Git repository, **Git will automatically use these global details**.  

---

## **Difference Between Local & Global Configuration**  

| Configuration Type | Scope | Use Case |
|-------------------|------|----------|
| **Local** | Applies only to a specific repository | If you work on different projects with different accounts |
| **Global** | Applies to all repositories on your system | If you use the same identity for all projects |

💡 **Pro Tip:** If you accidentally set the wrong name or email, simply run the same command with the correct details to **overwrite** the existing configuration.

---

## **Configuring Git on Different Operating Systems**  

### **Windows**  
✔ Install **Git for Windows** from [git-scm.com](https://git-scm.com/downloads).  
✔ Open **Git Bash** and run the configuration commands mentioned above.  

### **Mac (Using Homebrew)**  
✔ Install Git using Homebrew:  
  ```bash
  brew install git
  ```  
✔ Configure Git using the same commands:  
  ```bash
  git config --global user.name "Your Name"
  git config --global user.email "your-email@example.com"
  ```

### **Linux (Using APT or YUM)**  
✔ Install Git on **Debian-based (Ubuntu)** systems:  
  ```bash
  sudo apt install git
  ```  
✔ Install Git on **RHEL-based (CentOS, Fedora)** systems:  
  ```bash
  sudo yum install git
  ```  
✔ Configure Git globally:  
  ```bash
  git config --global user.name "Your Name"
  git config --global user.email "your-email@example.com"
  ```

---

## **Final Thoughts**  

Now that Git is **configured** on your system, every commit you make will be **attributed to you**. This is a crucial step in working effectively with Git, especially in **team projects** where tracking contributions is essential.  

✅ **You have successfully set up your Git identity!**  
📌 **Up Next:** Now that Git is configured, let’s learn how to initialize and work with Git repositories!  
