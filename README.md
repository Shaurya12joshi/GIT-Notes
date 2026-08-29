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


---

## 🙌 Credits

These notes were made while learning **Git & GitHub from CodeWithHarry**. Full credit goes to **CodeWithHarry** for the explanations and learning material used while creating these notes.

🎥 **Course / Video:**
https://www.youtube.com/watch?v=AB3J8ufDYHQ

