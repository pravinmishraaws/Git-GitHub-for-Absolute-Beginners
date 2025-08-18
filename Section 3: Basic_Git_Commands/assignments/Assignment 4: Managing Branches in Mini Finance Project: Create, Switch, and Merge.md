## **Title**  
Managing Branches in Mini Finance Project: Create, Switch, and Merge  

---

## **Description**  
In this assignment, you will **create, switch, and merge branches** for the **Mini Finance Project** to simulate real-world software development. You will work on a **feature update** in a separate branch, merge it into the main codebase, and ensure smooth version control.  

---

## **Estimated Duration**  
20-25 minutes  

---

## **Instructions**  

### **Scenario: Expanding the Mini Finance Project**  
You have joined the **Mini Finance** development team. Your task is to **add a new feature** to improve the project’s structure. Instead of working directly on the main branch, you will create a **feature branch**, implement changes, and merge them back into the main branch.

---

### **Step 1: Navigate to the Mini Finance Repository**  
Since we already created the **Mini Finance** repository in previous assignments, navigate to it:  

- **Windows (Command Prompt):**  
  ```
  cd path\to\Mini-Finance
  ```
- **Mac/Linux (Terminal):**  
  ```
  cd ~/path/to/Mini-Finance
  ```
- If unsure of your current directory, run:  
  ```
  pwd
  ```

---

### **Step 2: Check Your Current Branch**  
1️⃣ Verify the existing branches:  
   ```
   git branch
   ```
   **Expected Output:**  
   ```
   * master
   ```
   The `*` indicates you are on the `master` branch.

---

### **Step 3: Create and Switch to a Feature Branch**  
1️⃣ Create a new branch for your feature update:  
   ```
   git branch feature-budget-planner
   ```
2️⃣ Switch to the new branch:  
   ```
   git checkout feature-budget-planner
   ```
   or  
   ```
   git switch feature-budget-planner
   ```

3️⃣ Verify the active branch:  
   ```
   git branch
   ```
   **Expected Output:**  
   ```
     master
   * feature-budget-planner
   ```

---

### **Step 4: Modify Files in the Feature Branch**  
1️⃣ Open **index.html** and modify the `<h1>` tag:  
```html
<h1>Welcome to Mini Finance - Your Budgeting Companion</h1>
```
2️⃣ Open **style.css** and modify the body color:  
```css
body {
    font-family: Arial, sans-serif;
    background-color: #f8f9fa;
}
```
3️⃣ Save the changes.

---

### **Step 5: Stage and Commit Changes**  
1️⃣ Stage the modified files:  
   ```
   git add .
   ```
2️⃣ Commit the changes with a descriptive message:  
   ```
   git commit -m "Updated homepage heading and improved styling in feature-budget-planner branch"
   ```
3️⃣ Verify the commit history:  
   ```
   git log --oneline --decorate
   ```
   **Expected Output:**  
   ```
   9a6b7c8 (HEAD -> feature-budget-planner) Updated homepage heading and improved styling
   1a2b3c4 Initial commit - Added index.html and style.css
   ```

---

### **Step 6: Switch Back to the Master Branch**  
1️⃣ Move back to the **master** branch:  
   ```
   git checkout master
   ```
   or  
   ```
   git switch master
   ```
2️⃣ Open **index.html** and **style.css** again.  
   - **Notice:** The changes from `feature-budget-planner` **will not** be visible in `master`.

---

### **Step 7: Merge the Feature Branch into Master**  
1️⃣ Merge `feature-budget-planner` into `master`:  
   ```
   git merge feature-budget-planner
   ```
2️⃣ Open **index.html** and **style.css** again.  
   - **Now**, the changes should be **visible** in `master`!

---

### **Step 8: Verify the Merge**  
1️⃣ Check the commit history:  
   ```
   git log --oneline --decorate --graph
   ```
   **Expected Output:**
   ```
   *   8a9b0c1 (HEAD -> master) Merged feature-budget-planner into master
   |\  
   | * 9a6b7c8 (feature-budget-planner) Updated homepage heading and improved styling
   * | 1a2b3c4 Initial commit - Added index.html and style.css
   ```

---

### **Step 9: Clean Up (Optional)**  
1️⃣ Since `feature-budget-planner` is now merged, delete it:  
   ```
   git branch -d feature-budget-planner
   ```
2️⃣ Verify branch deletion:  
   ```
   git branch
   ```
   **Expected Output:**  
   ```
   * master
   ```

---

## **Questions**  
1. What is the purpose of creating a feature branch instead of working directly in `master`?  
2. How do you switch between branches in Git?  
3. What happens when you merge a branch into `master`?  
4. How does Git handle conflicts if the same file is modified in both `master` and `feature-budget-planner` before merging?  

---

## **Submission Requirements**  
Submit the following:  
✅ **Screenshot 1:** Output of `git branch` before creating a new branch.  
✅ **Screenshot 2:** Output of `git log --oneline --decorate` after committing changes in `feature-budget-planner`.  
✅ **Screenshot 3:** Output of `git log --oneline --decorate --graph` after merging `feature-budget-planner` into `master`.  
✅ **Text File (git_branching_summary.txt)** containing:  
   - A list of all Git commands used.  
   - A short explanation of what each command does.  

---

## **Solution**  
In case you're stuck, follow these correct solutions:

### **Step 1: Creating a Feature Branch**
```
git branch feature-budget-planner
git checkout feature-budget-planner
```

### **Step 2: Modifying Files**
```
echo "<h1>Welcome to Mini Finance - Your Budgeting Companion</h1>" > index.html
echo "body { background-color: #f8f9fa; }" > style.css
```

### **Step 3: Staging & Committing**
```
git add .
git commit -m "Updated homepage heading and improved styling in feature-budget-planner branch"
```

### **Step 4: Switching & Merging**
```
git checkout master
git merge feature-budget-planner
```

### **Step 5: Verifying & Cleaning**
```
git log --oneline --decorate --graph
git branch -d feature-budget-planner
```

✅ **By completing this assignment, you will gain hands-on experience in managing Git branches—a crucial skill for software development workflows.**
