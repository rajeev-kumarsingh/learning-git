# Day - 01 Tasks

- **Day 1:** What is Version Control, Git vs Other VCS, Installing Git

  - [Git Official Book: What is Git](https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control)
  - Practice: Install Git on your machine, configure name/email.

- **Day 2:** What is a Repository, git init, git config (local/global)
  - Practice: Initialize a local repo, configure VS Code Git integration.

**Day 3:** Working Directory, Staging Area, Committing Changes

- Practice: Create files, stage selectively, commit with clear messages.

---

```bash
git config --global user.name "rajeevsingh05"
git config --global user.email "rajeevsingh.devops@gmail.com" # You can share any email id not required to share git or gitlab email id

```

# Git Basic Commands

```bash
git init # Create local Repo
```

```bash
git status # List of untracted files
```

`O/P`

```bash
git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
  modified:   README.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
  git-github.pdf
  linux-git-schedule/
  linux_git_schedule.md

no changes added to commit (use "git add" and/or "git commit -a")
```

---

```bash
git add . # Add all modifies files to staging area
git add ./filename # Specific file goes into the staging area means git is just aware about the content of the file.
git add /relative-path/filename # Specific file goes into the staging area means git is just aware about the content of the file.
git status
```

`O/P`

```bash
git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
  modified:   README.md
  new file:   git-github.pdf
  new file:   linux-git-schedule/README.md
  new file:   linux_git_schedule.md
```

---

```bash
git rm --cached <file>... #To unstage
git rm -f -r --cached *

```

`O/P`

```bash
git rm -f -r --cached * # is used to remove files from the Git index (staging area) without deleting them from your working directory.
rm 'README.md'
rm 'git-github.pdf'
rm 'linux-git-schedule/README.md'
rm 'linux_git_schedule.md'
```

> `Note`: -f → force , Required when using git rm on files that are tracked and may have changes.
> `-r` → recursive, used to remove files inside directories. Without -r, git rm won’t remove folders or contents inside them. `--cached` Remove from Git index only (staging area). Files will remain in your local file system (they’re not deleted from your disk). `*` Wildcard: means all files and folders in the current directory.

---

Now check the status

```bash
git status
```

`O/P`

```bash
git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
  deleted:    README.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
  README.md
  git-github.pdf
  linux-git-schedule/
  linux_git_schedule.md
```

All tracked files now becomes untracked

```bash
git add .
git status
```

`O/P`

```bash
git add .
git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
  modified:   README.md
  new file:   git-github.pdf
  new file:   linux-git-schedule/README.md
  new file:   linux_git_schedule.md
```

---

```bash
git commit -m "type message here about your recent changes" #
```

## ![git-commit](gitcommit.png)

# Push the changes to GitHub Repository

```bash
git push origin main
```

> Output

```bash
git push origin main
Enter passphrase for key '/Users/rajeevsingh/.ssh/id_ed25519':
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 8 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (7/7), 362.62 KiB | 1.50 MiB/s, done.
Total 7 (delta 0), reused 0 (delta 0), pack-reused 0
To github.com:rajeev-kumarsingh/learning-git.git
   fd54e71..252ad48  main -> main
```

![gitpush](gitpush.png)
