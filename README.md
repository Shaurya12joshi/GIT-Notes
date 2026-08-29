# 🔀 Git

> **Git** — Version Control System

---

## 📚 Version Control Systems

Version control systems are of two types:

1. 🏢 **Centralised**
2. 🌐 **Distributed**

---

### 🏢 Centralised

* All history is stored on **one server**.
* ❌ Cannot be accessed offline.
* ⚠️ Problems related to the server will affect **all developers**.

---

### 🌐 Distributed

**Example:** Git

* Every developer has a **full copy of the project**.
* Changes are pushed to a **central/remote repository**.
* ⚡ Makes the system **fast**.
* 🛡️ Makes the system **reliable**.
* 👍 Makes the system **easy to use**.
* 📴 Can be used **offline**.
* 💾 Commits can be made offline.
* 🌐 Once the internet is available, the commits can be **pushed to the repository**.

# 🔀 Git vs GitHub

## 🔀 Git

* Git is a **version control system**.
* It **tracks changes in the codebase**.
* Basically, it converts folders into a **repository / `.git` directory**.
* You can see the **history of any repository** using Git.
* 💡 **In simple terms:** Git is software used to **track code history**.

---

## 🐙 GitHub

* GitHub is an **online platform where Git repositories are hosted**.
* Earlier, people had to create and manage **remote repositories** using Git, which could become complicated.
* GitHub was introduced to make this process easier by handling many of the complicated Git operations through its platform.
* GitHub became very popular, and **Microsoft acquired GitHub in 2018**.
* 🌐 **In simple terms:** GitHub is a platform to **host a repository online**.

### 🎥 Simple Analogy

> **GitHub is basically like YouTube for codebases.**

# ⚙️ Installing Git

Git can be used in **3 different ways**:

1. 💻 **Git using Command Line / Terminal** — Using Git commands in the terminal *(old method)*
2. 🧑‍💻 **Git using VS Code**
3. 🖥️ **Git using GitHub Desktop** — Through a GUI

---

## 📥 Installing Git

Install Git from here:

🔗 https://git-scm.com/install/

---

## ✅ Verify Git Installation

To verify if Git has been installed properly, run the command:

```bash
git --version
```

A **Git version number** will be displayed if Git is installed properly.

---

## 🚀 Initialising Git

To initialise Git in a project:

1. Open the **terminal**.
2. Navigate to a folder containing the codebase using basic `cd` commands.
3. Run the following command:

```bash
git init
```

This will initialise Git in the folder.

---

## 📊 Viewing Git Status

To view the **Git status of files**, run:

```bash
git status
```

# 🔄 How Git Works

There are **4 stages** in which our code stays:

1. 📁 **Working Directory**
2. 📦 **Staging Area**
3. 💾 **Local Repository**
4. 🌐 **Remote Repository**

---

## 🔁 Git Workflow

Once we initialise a Git repository in our codebase using:

```bash
git init
```

or clone an existing repository using:

```bash
git clone <url>
```

we will have a **Git repository in our codebase**.

If we make any changes, we should move the codebase to the **Staging Area** using the `git add` command.

```bash
git add
```

Doing this, the code files are now added to the **Staging Area**.

Next, we **commit the code files** with a commit message so that others can understand the changes that we made in the code files.

Commit is done using:

```bash
git commit
```

Next, we **push the changes to the Remote Repository** using:

```bash
git push
```

To get the changes made by our **co-workers**, we use:

```bash
git pull
```

---

## 📌 Git Workflow at a Glance

```text
Working Directory
       ↓
   git add
       ↓
Staging Area
       ↓
  git commit
       ↓
Local Repository
       ↓
   git push
       ↓
Remote Repository
       ↓
   git pull
       ↓
Working Directory
```

# ⚙️ Configure Your Username and Email

To update / set your **username**:

```bash
git config --global user.name "Your_Name"
```

To update / set your **email**:

```bash
git config --global user.email "Your_Email"
```

---

# 🛠️ Big 4 Git Commands

### 1. `git init`

Used for **initialising Git in a codebase**.

Git starts tracking the codebase after this.

```bash
git init
```

---

### 2. `git status`

Used to view:

* Which files are being tracked
* Which files have been changed
* Which files are in the **Staging Area**
* Which files are in the Staging Area but **not committed**

```bash
git status
```

---

### 3. `git add`

Used to add files to the **Staging Area**.

```bash
git add <file_name>
```

---

### 4. `git commit`

Used to commit files with a **commit message** so others can understand what changes you made.

```bash
git commit -m "Commit_Msg"
```

---

# 💡 Tip

Enable **hidden folders/files** to view the `.git` folder.

⚠️ **Do not make any changes inside the `.git` folder.**

---

# 📜 Viewing Commit History

### `git log`

Used to see **who made what commit and at what date and time**.

```bash
git log
```

### `git log --oneline`

Used to view a **concise summary** of the information available with the `git log` command.

```bash
git log --oneline
```
# 🌿 Branching

**Branching** is done when you don't want to disturb the work being done in the **main branch**, but still want to build on the same codebase.

A new branch allows you to work separately from the main branch. Once the work is complete, the branch can later be **merged back into the main branch**.

```text
              ┌── Feature Branch ──→ Merge
             /                       ↓
Main ───────●────────────────────────●
```

---

## 🌱 Create a New Branch

To create a new branch:

```bash
git branch NameOfBranch
```

---

## 🔄 Switch Between Branches

To switch from one branch to another:

```bash
git switch NameOfBranch
```

---

## 🔀 Merge a Branch

To merge a branch into the **main branch**:

1. First switch to the **main branch**.
2. Then merge the required branch.

```bash
git switch main
```

```bash
git merge NameOfBranch
```

---

## 🗑️ Delete a Branch

To delete a branch:

```bash
git branch -d NameOfBranch
```

# ⚔️ Merge Conflicts

A **merge conflict** occurs when Git cannot automatically combine changes from two branches.

This commonly happens when the **same file has been changed in different ways** in two branches.

For example:

```text id="m8f4qk"
main branch
    │
    └── app.js
         │
         └── balance = 100

feature branch
    │
    └── app.js
         │
         └── balance = 500
```

If both branches changed the same part of `app.js` and we try to merge them, Git may not know **which change should be kept**.

---

## 🚨 What Happens During a Conflict?

When Git encounters a conflict, the merge is stopped and Git marks the conflicting section in the file.

It may look something like this:

```text id="9y2k6w"
<<<<<<< HEAD
balance = 100
=======
balance = 500
>>>>>>> feature
```

The markers indicate:

* `<<<<<<< HEAD` → Changes from the branch you are currently on
* `=======` → Separates the two versions
* `>>>>>>> feature` → Changes coming from the branch being merged

---

## 🛠️ How to Resolve a Merge Conflict

A person has to **manually inspect the conflicting code** and decide what should be kept.

You can:

* ✅ Keep the changes from the current branch
* ✅ Keep the changes from the other branch
* 🔀 Keep parts of both changes
* ✏️ Write a completely different solution

After deciding what should remain, remove the conflict markers and save the file.

Then the resolved file needs to be added to the **Staging Area**:

```bash
git add <file_name>
```

After all conflicts have been resolved and staged, complete the merge with a commit:

```bash
git commit
```

---

## 🧠 Important Point

Git can automatically merge many changes when they affect different parts of a file.

A **merge conflict does not mean Git is broken**. It simply means Git needs a human to decide **which version of the conflicting code is correct**.

> **Git can detect the conflict, but the developer has to decide how it should be resolved.**

---

## 🔄 Conflict Resolution Flow

```text
Merge Branches
      ↓
Git Detects Conflict
      ↓
Merge Paused
      ↓
Manually Inspect Conflicting Files
      ↓
Choose / Combine Changes
      ↓
Remove Conflict Markers
      ↓
git add
      ↓
git commit
      ↓
✅ Merge Completed
```
# 📦 Stashing

**Stashing** is useful when you have a lot of files being edited, but suddenly need to make an **emergency or high-priority change**.

Instead of committing your unfinished work, you can **stash** the changes.

Stashing temporarily stores your uncommitted changes in a separate place and makes your **working directory clean**, allowing you to work on something else.

You can also store **multiple sets of changes** in the stash.

---

## 📥 Add Changes to Stash

To stash your current changes:

```bash
git stash
```

This temporarily stores your changes and cleans your working directory.

---

## 📋 View Stashed Changes

To view the changes currently saved in the stash:

```bash
git stash list
```

---

## ♻️ Restore Stashed Changes

To restore the most recent stashed changes and **remove them from the stash**:

```bash
git stash pop
```

---

## 🔄 Apply Stashed Changes

To restore the stashed changes while **keeping them in the stash**:

```bash
git stash apply
```

### 🆚 `git stash pop` vs `git stash apply`

| Command           | Restores Changes | Keeps Changes in Stash |
| ----------------- | :--------------: | :--------------------: |
| `git stash pop`   |         ✅        |            ❌           |
| `git stash apply` |         ✅        |            ✅           |

---

# 🌿 Best Practices for Branching

### 1. 🎯 One Feature → One Branch

Create a separate branch for each feature or piece of work.

```text
Feature A → Branch A
Feature B → Branch B
Feature C → Branch C
```

---

### 2. 🚫 Never Develop Directly on `main`

Avoid making your development changes directly on the **main branch**.

Instead, create a separate branch and merge it into `main` once the work is ready.

---

### 3. 🗑️ Delete the Branch Once Merged

Once a branch has been successfully merged into `main`, delete it if it is no longer needed.

```bash
git branch -d NameOfBranch
```

---

### 4. 🏷️ Use Meaningful Branch Names

Use branch names that clearly describe what you are working on.

For example:

```text
feature/login
feature/payment
fix/navbar
fix/authentication
```

---

### 5. ⏱️ Keep Branches Short-Lived

Avoid keeping branches open for a long period of time.

**Merge branches as soon as the work is ready** to reduce the chances of conflicts and keep the codebase easier to manage.

---

## 🧠 Quick Summary

```text
🌿 Branching
     ↓
Work on a Feature
     ↓
📦 Need to switch urgently?
     ↓
git stash
     ↓
Working Directory becomes clean
     ↓
🚨 Handle Priority Work
     ↓
git stash pop / git stash apply
     ↓
Continue Your Work
```
# 🏷️ Git Tags

Git **tags** are used to mark a specific commit in the repository.

They are commonly used to mark important points in a project's history, such as a **release or version**.

For example:

```text
v1.0.0
v1.1.0
v2.0.0
```

---

## 📌 Types of Git Tags

There are **2 types of tags in Git**:

1. 📝 **Annotated Tags**
2. 🏷️ **Lightweight Tags**

---

## 📝 1. Annotated Tag

An **annotated tag** is a tag that contains additional information such as:

* Tag name
* Tag message
* Tagger information
* Date

It is useful for marking **important releases** because the tag contains information about why it was created.

### Creating an Annotated Tag

First, **commit your changes**.

Then create the tag:

```bash
git tag -a v1.x.x -m "Tag Message"
```

For example:

```bash
git tag -a v1.0.0 -m "First Release"
```

---

## 🏷️ 2. Lightweight Tag

A **lightweight tag** is a simple pointer to a specific commit.

It does not contain the additional information that an annotated tag stores.

### Creating a Lightweight Tag

```bash
git tag v1.x.x
```

For example:

```bash
git tag v1.0.0
```

---

## 🔍 View Tags

To view the tags created in the repository:

```bash
git tag
```

Example output:

```text
v1.0.0
v1.1.0
v2.0.0
```

---

## 🆚 Annotated vs Lightweight

|                          | 📝 Annotated | 🏷️ Lightweight |
| ------------------------ | ------------ | --------------- |
| Additional information   | ✅ Yes        | ❌ No            |
| Tag message              | ✅ Yes        | ❌ No            |
| Simple pointer to commit | ❌            | ✅               |
| Useful for releases      | ✅            | ✅               |

### 💡 Simple Way to Remember

> **Annotated Tag** → A tag with information attached to it.

> **Lightweight Tag** → A simple name pointing to a commit.


---

## 🙌 Credits

These notes were made while learning **Git & GitHub from CodeWithHarry**. Full credit goes to **CodeWithHarry** for the explanations and learning material used while creating these notes.

🎥 **Course / Video:**
https://www.youtube.com/watch?v=AB3J8ufDYHQ

