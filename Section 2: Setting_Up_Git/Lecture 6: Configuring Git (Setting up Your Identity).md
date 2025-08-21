# Lab – Configuring Git (Setting up Your Identity)

## 1. Why Configure Git?

* Every time you make a commit, Git saves:

  * **Author’s Name**
  * **Author’s Email**
* This information appears in the **commit history**, helping teams know **who made which change**.
* Without setting this up, Git won’t allow you to commit properly.

---

## 2. Setting Your Identity

### Step 1: Set Your Name

```bash
git config --global user.name "Your Name"
```

* Example:

  ```bash
  git config --global user.name "Pravin Mishra"
  ```

### Step 2: Set Your Email

```bash
git config --global user.email "your.email@example.com"
```

* Example:

  ```bash
  git config --global user.email "pravin@example.com"
  ```

💡 Use the **same email linked to your GitHub account** if you plan to push code to GitHub.

---

## 3. Verifying Configuration

```bash
git config --list
git config --list --show-origin   # where a value comes from
git config --global --list        # global list
git config --local --list         # local list

```

* Shows all Git configurations (name, email, editor, etc.).
* You should see your username and email listed.

---

## 4. Local vs Global Configuration

* `--global` → applies to **all repositories** on your computer.
* `--local` → applies only to the **current repository**.
* Example (local config inside a repo):

  ```bash
  git config --local user.name "Project-Specific Name"
  ```

---

## 5. Common Extra Configurations (Optional but Useful)

* **Default Editor** (e.g., VS Code):

  ```bash
  git config --global core.editor "code --wait"
  ```
**What it does**

Tells Git which text editor to open when it needs your input.

Common scenarios:
- Writing a commit message (if you don’t use -m "msg").
- Editing a merge conflict.
- Rebase operations (when Git needs you to reorder/edit commits).

By default, Git often uses Vim — which many beginners find intimidating.
Setting it to VS Code (or your favorite editor) makes things much easier.

code --wait = tells VS Code to open the file and pause Git until you close it.

* **Colored Output** for better readability:

  ```bash
  git config --global color.ui auto
  ```

**What it does**

Adds syntax highlighting & colors to Git’s terminal output.

Example:

- Branch names in green/yellow
- Added lines in green
- Removed lines in red
- Merge conflicts in highlighted sections

This makes Git’s output easier to read, especially when scanning diffs, logs, or status messages.

---

## 6. Example Workflow

1. You create a new Git repository.
2. Before committing, you configure:

   ```bash
   git config --global user.name "Alice Johnson"
   git config --global user.email "alice@example.com"
   ```
3. Now every commit will be tagged with **Alice Johnson [alice@example.com](mailto:alice@example.com)**.

---

### Key Takeaway:
✅  Configuring Git ensures your commits are properly attributed to you. Use `--global` for all projects, or `--local` for project-specific identities.

