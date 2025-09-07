# Assignment 9: Collaborating on Mini-Finance with GitHub

## Objective
In this assignment, you’ll simulate a real-world **collaborative GitHub workflow** using the `mini_finance` project.  
You will practice:  
- Authenticating to GitHub from the command line  
- Creating and cloning a remote repository  
- Making and pushing code changes  
- Pulling updates from upstream  
- Opening a Pull Request  

---

## Learning Objectives
By the end of this assignment, you will be able to:
- Authenticate to GitHub (SSH or HTTPS)  
- Create a fork of a repository  
- Clone a repo locally and configure remotes  
- Create a feature branch, commit changes, and push  
- Open a Pull Request (PR)  

---

## Step 0 — Access Existing Mini-Finance Code
The upstream repository exists at:  
👉 [https://github.com/pravinmishraaws/mini_finance](https://github.com/pravinmishraaws/mini_finance)  

You will **fork this repo**, then work on your own copy.  

---

## Step 1 — Fork & Authenticate

1. Login to GitHub and **Fork** the `mini_finance` repo into your account.  
2. In your terminal, configure authentication:  

### SSH (Recommended)
```bash
ssh-keygen -t ed25519 -C "your.email@example.com"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
````

* Copy the contents of `~/.ssh/id_ed25519.pub` into GitHub → **Settings → SSH and GPG keys**

Force Git to use SSH:

```bash
git config --global url."git@github.com:".insteadOf "https://github.com/"
```

### HTTPS (Alternative)

```bash
git config --global credential.helper cache
```

### Test Authentication

```bash
git ls-remote git@github.com:yourusername/mini_finance.git
```

✅ **Expected Outcome:** You have forked the repo, and your terminal is authenticated for Git operations.

---

## Step 2 — Clone Your Fork Locally

```bash
git clone git@github.com:yourusername/mini_finance.git
cd mini_finance
git remote -v
```

* `origin` → your fork
* Add an `upstream` remote to the original repo:

```bash
git remote add upstream https://github.com/pravinmishraaws/mini_finance.git
```

✅ **Expected Outcome:** Local clone has **origin** (your fork) and **upstream** (original repo).

---

## Step 3 — Create a Feature Branch & Make a Change

Create a new branch:

```bash
git checkout -b feature-readme-update
```

Edit `README.md` → add this new section:

```markdown
## About This Project
This project demonstrates Git operations like clone, pull, push, and PR — a hands-on Mini-Finance tool.
```

Stage & commit:

```bash
git add README.md
git commit -m "docs: update README with assignment note"
```

---

## Step 4 — Pull From Upstream & Push to Origin

Sync changes from upstream:

```bash
git fetch upstream
git checkout main
git merge upstream/main
```

Switch back to your feature branch:

```bash
git checkout feature-readme-update
git rebase main   # optional but recommended
```

Push your branch:

```bash
git push -u origin feature-readme-update
```

✅ **Expected Outcome:** Your branch is available on GitHub under your fork.

---

## Step 5 — Create a Pull Request

1. Go to your fork on GitHub
2. Click **Compare & Pull Request**
3. Target: `pravinmishraaws/mini_finance:main` ← from `yourusername:feature-readme-update`
4. Title:

   ```
   docs: update README with assignment note
   ```
5. Description:

   ```
   This PR adds a new section to the README explaining the project's purpose in the context of this GitHub assignment.
   ```
6. Submit the Pull Request.

---

## How to Submit Your Assignment

### For Live Cohort Students

Follow the submission guidelines explained during the live session.

DevOps Micro Internship [Assignment Master Sheets](https://docs.google.com/spreadsheets/d/1HnlenHEjytvLJMy84bBF-5B1RABaY_BjbfwCj-qnvHM/edit?gid=1951781267#gid=1951781267)


### For Self-Paced Udemy Students

Submit the assignment by clicking **“Next”** and answering the provided questions.

---

## Questions for This Assignment

### 1. Fork & Clone (Screenshot + Explanation)

* **Screenshot A:** GitHub page showing your **forked mini\_finance repo** (URL visible)
* **Screenshot B:** Terminal output of `git remote -v` showing both **origin** and **upstream**
* **Text (1–2 lines):** What is the purpose of the `upstream` remote in your workflow?

---

### 2. Branching, Rebase, Push (Screenshot + Explanation)

* **Screenshot C:** Terminal showing your commit on `feature-readme-update`

  ```bash
  git log --oneline -n 3
  ```
* **Screenshot D:** Confirmation of `git push -u origin feature-readme-update`
* **Text (1–2 lines):** Why did you rebase or merge from `upstream/main` before pushing?

---

### 3. Pull Request (Screenshot + Text)

* **Screenshot E:** GitHub UI showing your **open Pull Request** (title + description visible)
* **Text (1–2 lines):** Why is creating a Pull Request an important step in team collaboration?

