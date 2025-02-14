### **Title:**  
Uploading and Syncing the Mini Finance Project with GitHub  

---

### **Description:**  
In this assignment, you will link your **local Mini Finance repository** to a **GitHub remote repository**, upload your project files using `git push`, and ensure synchronization using `git pull`. This assignment will help you understand **collaborative workflows** and how to manage code versions across multiple systems.  

---

### **Estimated Duration:**  
20-30 minutes  

---

## **Instructions**  

### **Step 1: Link Local Repository to GitHub**  
In the previous assignment, you created a **Mini-Finance repository on GitHub**. Now, let's link it with your local repository.  

1️⃣ Navigate to your **local Mini-Finance project** directory:  

```sh
cd path/to/Mini-Finance
```  

2️⃣ Verify your local repository by checking the Git status:  

```sh
git status
```  

3️⃣ Add a **remote repository link** to connect GitHub to your local Git:  

```sh
git remote add origin <your-repository-URL>
```  

4️⃣ Verify that the remote repository has been added successfully:  

```sh
git remote -v
```  

✅ **Expected Outcome:** The output should display your GitHub repository URL linked under `origin`.  

---

### **Step 2: Upload Local Files to GitHub**  
Now that your local Mini-Finance repository is linked to GitHub, let's push the existing files.  

1️⃣ Stage all the files in the repository:  

```sh
git add .
```  

2️⃣ Commit the changes with a meaningful message:  

```sh
git commit -m "Initial commit of Mini Finance project"
```  

3️⃣ Push the changes to GitHub:  

```sh
git push -u origin master
```  

✅ **Expected Outcome:** All local files are uploaded to the GitHub repository.  

---

### **Step 3: Sync Changes Between Local and Remote Repository**  
After pushing changes, let’s ensure you can **pull any future updates** from GitHub.  

1️⃣ Modify any file (e.g., update `index.html`) **directly on GitHub**.  
2️⃣ Use `git pull` to fetch those changes locally:  

```sh
git pull origin master
```  

✅ **Expected Outcome:** Any changes made on GitHub should now be reflected in your local repository.  

---

## **Questions**  

1. What does `git remote add origin <URL>` do?  
2. What is the purpose of `git push -u origin master`?  
3. How does `git pull` help maintain synchronization?  
4. What happens if two people make conflicting changes in the same file?  
5. How can you check which remote repository your local Git is connected to?  

---

## **Submission Requirements**  

✅ **Screenshot 1:** Output of `git remote -v` showing the linked GitHub repository.  
✅ **Screenshot 2:** Output of `git push`, confirming files were uploaded to GitHub.  
✅ **Screenshot 3:** Output of `git pull`, verifying successful synchronization.  
✅ **Text File (github_sync_summary.txt)** containing:  
   - A list of **commands used** with a brief explanation.  
   - Answers to the **questions**.  

---

## **Solution**  

### **Step 1: Link Local Repository**  
- `git remote add origin <URL>` → Links local repository to GitHub.  
- `git remote -v` → Confirms the connection.  

### **Step 2: Push Local Files to GitHub**  
- `git add .` → Stages all files.  
- `git commit -m "Initial commit"` → Saves changes locally.  
- `git push origin master` → Uploads files to GitHub.  

### **Step 3: Syncing Local and Remote**  
- `git pull origin master` → Fetches remote changes.  

✅ **By completing this assignment, you have successfully linked, uploaded, and synchronized the Mini Finance Project with GitHub!**  
