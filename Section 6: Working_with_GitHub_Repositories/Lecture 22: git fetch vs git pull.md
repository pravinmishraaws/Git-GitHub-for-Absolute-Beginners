# Hands-On Lab: `git fetch` vs `git pull` with Mini-Finance Project

**Goal:** Understand the difference between `git fetch` and `git pull` by practicing both commands and seeing their impact on local and remote branches.

---

## 1️⃣ Lab Setup

### Step 1: Fork & Clone Mini-Finance Repo

1. Fork [Mini-Finance Repo](https://github.com/pravinmishraaws/mini_finance) to your GitHub account.
2. Clone it locally:

```bash
git clone https://github.com/<your-username>/mini_finance.git
cd mini_finance
```

3. Add the original repo as upstream:

```bash
git remote add upstream https://github.com/pravinmishraaws/mini_finance.git
git remote -v
```

**Expected:**

* `origin` → your fork
* `upstream` → original repo

---

## 2️⃣ Simulating Remote Changes

We need some changes on `upstream` (original repo).

* Imagine a teammate commits a change directly to `upstream/main` (you can simulate this if you have two accounts or instructor does this).

Now your **local main** is behind **upstream/main**.

---

## 3️⃣ Using `git fetch`

```bash
# Get remote changes from upstream without merging
git fetch upstream main
```

**What happened?**

* Downloads commits from `upstream/main`.
* Updates `upstream/main` pointer.
* **Does not touch your local `main` or working files.**

Check commits that are on `upstream/main` but not on your `main`:

```bash
git log main..upstream/main --oneline
```

**Expected Output:**

```
a1b2c3d Added login feature
b4c5d6e Fixed header styling
```

**Explanation:**

* These commits exist on `upstream/main`.
* Your local `main` hasn’t changed yet — safe to inspect before merging.

---

## 4️⃣ Merging After Fetch (Optional)

If you’re ready to apply changes:

```bash
git merge upstream/main
```

**Now your local `main` is updated** with remote commits.

---

## 5️⃣ Using `git pull`

Alternatively, you could have used:

```bash
git pull upstream main
```

**What happened?**

* `git fetch` → downloads changes
* `git merge` → applies them immediately to your local branch

Check history:

```bash
git log --oneline
```

Your local branch now contains remote commits automatically.

---

## 6️⃣ Key Difference (Quick Table)

| Feature               | `git fetch`                     | `git pull`                         |
| --------------------- | ------------------------------- | ---------------------------------- |
| Downloads commits?    | ✅ Yes                           | ✅ Yes                              |
| Updates local branch? | ❌ No (only updates remote refs) | ✅ Yes (merges into current branch) |
| Safe to inspect?      | ✅ Yes, inspect first            | ❌ No, merges immediately           |
| Typical use case      | Review changes before merging   | Quick sync with remote             |

---

## 7️⃣ Recommended Workflow

**Safer approach for teams:**

```bash
# Step 1: See remote changes
git fetch upstream main
git log main..upstream/main --oneline

# Step 2: Merge when ready
git merge upstream/main
```

**Shortcut if confident:**

```bash
git pull upstream main
```

---

## 8️⃣ Visual Diagram

```
Before Fetch:           After Fetch:            After Pull:
 Local main              Local main             Local main
    |                       |                     |
    o---o (commits)          o---o                 o---o---o---o (merged)
                            Upstream/main → o---o---o---o
```
