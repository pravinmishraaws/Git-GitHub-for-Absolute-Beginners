# Assignment 7: Branching Workflow — Add & Verify a Contact Page

## Objective
This assignment builds on your **previous CodeTrack project** and will help you practice:  
- Creating a branch  
- Switching between branches  
- Committing changes  
- Merging to main  
- Verifying changes via a live link  

---

## Step 0 — Start from Your Existing Repo
Navigate to your CodeTrack project:
```bash
cd path/to/CodeTrack
git status
git branch
````

✅ Ensure you are on the **main** (or master) branch.

---

## Step 1 — Create and Switch to a Feature Branch

```bash
git checkout -b feature/contact-page
git branch
```

**Expected Output:**

```
* feature/contact-page
  main
```

---

## Step 2 — Add `contact.html` (in the branch)

### Create the file

```bash
# macOS/Linux
touch contact.html

# Windows PowerShell
ni contact.html
```

### Add content to `contact.html`

```html
<!doctype html>
<html>
<head>
  <meta charset="utf-8">
  <title>Contact - CodeTrack</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>Contact Us</h1>
  <p>Email: mail@pravinmishra.in</p>
  <p>Website: https://thecloudadvisory.com/</p>
</body>
</html>
```

### Stage & commit

```bash
git add contact.html
git commit -m "feat(contact): add contact page with email and website"
```

---

## Step 3 — Add a Link in `index.html` (still on the branch)

Insert this paragraph **below the existing playlist paragraph**:

```html
<p class="playlist-line">
    If you’d like to learn more, check out the playlist:
    <a href="https://www.youtube.com/playlist?list=PLVOdqXbCs7bX88JeUZmK4fKTq2hJ5VS89" target="_blank">
        DevOps for Beginners – Free Playlist
    </a>
</p>

<!-- ADD THIS NEW PARAGRAPH RIGHT BELOW THE ONE ABOVE -->
<p class="playlist-line">
    Want to reach us? Visit the
    <a href="contact.html">Contact Page</a>.
</p>
```

### Stage & commit

```bash
git add index.html
git commit -m "feat(nav): add Contact Page link to index.html"
```

---

## Step 4 — Verify Isolation (Switch Back to Main)

```bash
git checkout main
ls
```

* `contact.html` should **not** be in main yet.
* Open `index.html` in a browser → the **Contact Page link should not exist**.

👉 This proves your changes live only in the feature branch.

---

## Step 5 — Merge the Feature Branch into Main

```bash
git merge feature/contact-page
```

Now verify:

* Run `ls` → `contact.html` should be present.
* Open `index.html` in a browser → you should now see the **Contact Page link**.
* Click the link → it should open `contact.html`. ✅

---

## Step 6 — Inspect History (Graph View)

```bash
git log --oneline --graph --decorate --all
```

(Optional cleanup):

```bash
git branch -d feature/contact-page
```

---

## How to Submit Your Assignment

### For Live Cohort Students

Please follow the submission guidelines explained during the live session.

DevOps Micro Internship [Assignment Master Sheets](https://docs.google.com/spreadsheets/d/1HnlenHEjytvLJMy84bBF-5B1RABaY_BjbfwCj-qnvHM/edit?gid=1951781267#gid=1951781267)


### For Self-Paced Udemy Students

Submit the assignment by clicking **“Next”** and answering the provided questions.
