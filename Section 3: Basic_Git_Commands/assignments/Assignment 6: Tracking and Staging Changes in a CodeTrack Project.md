# Assignment 6: Tracking and Staging Changes in a CodeTrack Project

## Objective
This assignment will reinforce the concepts from **Section 3: Basic Git Commands** by requiring you to:  
- Create and track files in Git  
- Stage changes using `git add`  
- Verify the status using `git status`  
- Commit changes  
- Deploy the project on an EC2 instance  

---

## Step 1: Ensure Your Git Setup
Before proceeding, make sure that:  
- Git is **installed** on your system  
- Git is properly **configured** with your username and email  

---

## Step 2: Navigate to the Project Folder

Since you already created the **CodeTrack Project Folder** in the last assignment, navigate to it:

### Windows (Command Prompt)
```cmd
cd path\to\CodeTrack
````

### macOS/Linux (Terminal)

```bash
cd ~/path/to/CodeTrack
```

Check current directory:

```bash
pwd
```

---

## Step 3: Create and Modify Files

Create two new files:

```bash
touch index.html style.css
```

👉 For Windows users without `touch`:

```cmd
echo > index.html
echo > style.css
```

Verify creation:

```bash
ls
```

**Expected Output:**

```
index.html
style.css
```

### Modify Files

1. Open `index.html` and `style.css` in a text editor.
2. Go to GitHub and open the repository: **[Week-2---Git-GitHub-Assignment](https://github.com/pravinmishraaws/Week-2---Git-GitHub-Assignment)**
3. Copy the content from both files and paste them into your local files.

---

## Step 4: Track the Files Using Git

Check repository status:

```bash
git status
```

**Expected Output:**
Files `index.html` and `style.css` listed as **untracked**.

Stage files:

```bash
git add .
# OR
git add index.html
git add style.css
```

Verify staging:

```bash
git status
```

**Expected Output:**
Files listed under **Changes to be committed**.

---

## Step 5: Commit the Changes

Commit with a meaningful message:

```bash
git commit -m "Initial commit - Added index.html and style.css"
```

**Expected Output:**

```
[master (root-commit) 1a2b3c4] Initial commit - Added index.html and style.css
 2 files changed, 10 insertions(+), 0 deletions(-)
```

Verify commit history:

```bash
git log --oneline
```

**Expected Output:**

```
1a2b3c4 Initial commit - Added index.html and style.css
```

---

## Step 6: Modify a File and Commit Again

Open `index.html` in a browser → follow the instructions written inside.

![2025-08-19_14-55-17-4999df1a56473cb3d1031d4fbe21f41f](https://github.com/user-attachments/assets/e838010a-3259-4a5c-9407-b290737bd427)

Check repo status:

```bash
git status
```

Stage modified file:

```bash
git add index.html
```

Commit changes with a meaningful message:

```bash
git commit -m "Updated heading in index.html"
```

Verify history:

```bash
git log --oneline
```

**Expected Output:**

```
3d4e5f6 Updated heading in index.html
1a2b3c4 Initial commit - Added index.html and style.css
```

---

## Step 7: Deploy Application on an EC2 Instance

1. **Launch** an EC2 Instance
2. **Connect** via SSH:

   ```bash
   ssh -i your-key.pem ec2-user@<EC2-Public-IP>
   ```
3. **Update packages**:

   ```bash
   sudo yum update -y    # Amazon Linux
   # OR
   sudo apt update -y    # Ubuntu
   ```
4. **Install Nginx**:

   ```bash
   sudo yum install -y nginx   # Amazon Linux
   sudo apt install -y nginx   # Ubuntu
   ```
5. **Start Nginx**:

   ```bash
   sudo systemctl start nginx
   sudo systemctl enable nginx
   ```
6. **Deploy your application**:
   Copy project files (`index.html`, `style.css`) into Nginx’s web directory:

   ```bash
   sudo cp index.html style.css /usr/share/nginx/html/
   ```
7. **Access Application**:
   Open a browser:

   ```
   http://<EC2-Public-IP>
   ```

You should see your application running successfully 🎉

---

## How to Submit Your Assignment

### For Live Cohort Students

Follow the submission guidelines explained during the live session.

DevOps Micro Internship [Assignment Master Sheets](https://docs.google.com/spreadsheets/d/1HnlenHEjytvLJMy84bBF-5B1RABaY_BjbfwCj-qnvHM/edit?gid=1951781267#gid=1951781267)

### For Self-Paced Udemy Students

Submit the assignment by clicking **“Next”** and answering the provided questions.
