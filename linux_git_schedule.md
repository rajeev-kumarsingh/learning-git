## 30-Day Linux Git & GitHub Real-World Practice Schedule (1.5-2 hr/day)

This plan follows the **Git & GitHub roadmap** from your PDF with **real-world practice** and **resource links**, enabling you to complete it in **30 days**, aligned for **practical DevOps / CI/CD readiness**.

---

### **Week 1: Core Git Basics & Local Workflow**

- **Day 1:** What is Version Control, Git vs Other VCS, Installing Git
  - [Git Official Book: What is Git](https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control)
  - Practice: Install Git on your machine, configure name/email.

- **Day 2:** What is a Repository, git init, git config (local/global)
  - Practice: Initialize a local repo, configure VS Code Git integration.

- **Day 3:** Working Directory, Staging Area, Committing Changes
  - Practice: Create files, stage selectively, commit with clear messages.

- **Day 4:** .gitignore, Viewing Commit History
  - [Gitignore Templates](https://github.com/github/gitignore)
  - Practice: Create `.gitignore` for Node/Python, view logs with `git log`, `git log --oneline`.

- **Day 5:** Branching Basics (create, rename, delete, checkout, merge)
  - [Git Branching](https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell)
  - Practice: Create feature branches, merge back, handle basic conflicts.

- **Day 6:** Basic Collaboration Concepts
  - Practice: Use a dummy project to simulate feature branch workflows.

- **Day 7:** Recap + Mini Project: Create a simple CLI app/script and manage it with Git locally.

---

### **Week 2: GitHub Essentials & Collaboration**

- **Day 8:** Creating GitHub Account, GitHub Interface, Profile Readme
  - [Create Profile Readme](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-github-profile/customizing-your-profile/about-your-profile)

- **Day 9:** Creating Repositories, Private vs Public, Git Remotes
  - Practice: Create a new repo, link your local repo, push changes.

- **Day 10:** Managing Remotes, Pushing/Pulling, Fetch without Merge
  - Practice: `git remote add`, `git push`, `git pull`, `git fetch` + `git merge`.

- **Day 11:** Forking vs Cloning, Collaboration, Issues
  - [GitHub Forks](https://docs.github.com/en/get-started/quickstart/fork-a-repo)
  - Practice: Fork a public repo, clone locally, push changes.

- **Day 12:** Pull Requests (PR), PR from Fork, Labelling Issues/PRs
  - [Creating Pull Requests](https://docs.github.com/en/pull-requests)
  - Practice: Create a PR on a forked repo, review, request changes.

- **Day 13:** Merge Strategies (Fast-forward, Non-FF), Handling Conflicts
  - Practice: Create merge conflicts, resolve them, merge PRs.

- **Day 14:** Recap + Mini Project: Fork an open-source repo, make small enhancements, and open a PR.

---

### **Week 3: Advanced Git Topics for Real-World Scenarios**

- **Day 15:** Git Stash, HEAD, Detached HEAD, git log options
  - Practice: Use `git stash` to switch tasks, experiment with `HEAD`, recover from detached states.

- **Day 16:** Undoing Changes (`git revert`, `git reset` with --soft, --hard, --mixed)
  - Practice: Safely undo commits, understand reset types.

- **Day 17:** Viewing Diffs, Between Branches, Commits
  - Practice: Use `git diff`, `git diff branch1..branch2`.

- **Day 18:** Rewriting History (commit --amend, rebase, filter-branch)
  - [Rebase Guide](https://www.atlassian.com/git/tutorials/rewriting-history)
  - Practice: Squash commits, rebase feature branches.

- **Day 19:** Tagging & Releases, Managing Tags, Checkout Tags
  - Practice: Create annotated tags, push tags to GitHub, understand release workflow.

- **Day 20:** GitHub Releases, Git Hooks Basics (pre-commit, commit-msg)
  - Practice: Create a GitHub release, set up a `pre-commit` hook.

- **Day 21:** Recap + Mini Project: Version your CLI app with tags and GitHub releases, use a pre-commit hook for linting.

---

### **Week 4: GitHub Actions & Advanced Workflow**

- **Day 22:** GitHub CLI, Installation, Repo Management
  - [GitHub CLI](https://cli.github.com/)
  - Practice: Manage issues, PRs from CLI.

- **Day 23:** GitHub Actions, YAML Syntax, Workflow Triggers
  - [GitHub Actions Docs](https://docs.github.com/en/actions)
  - Practice: Create a simple CI workflow that lints and runs tests.

- **Day 24:** Workflow Runners, Context, Secrets & Env Vars
  - Practice: Add secrets, run workflows using them.

- **Day 25:** Caching, Storing Artifacts, Workflow Status
  - Practice: Cache dependencies in workflows.

- **Day 26:** Marketplace Actions, Automation Use Cases
  - Practice: Use marketplace actions for linting/testing.

- **Day 27:** Git Patch, Git Reflog, Git Bisect, Worktree
  - Practice: Use `git reflog` for recovery, `git bisect` for bug tracing.

- **Day 28:** GitHub Pages, Gists, Packages
  - Practice: Deploy a static portfolio page using GitHub Pages.

- **Day 29:** Contribution Guidelines, Clean Git History, Markdown
  - Practice: Add `CONTRIBUTING.md`, clean history, document README.md.

- **Day 30:** **Capstone Project Day**
  - Create a simple project with GitHub Actions CI, proper branching, PR workflow, tags/releases, and GitHub Pages for documentation.
  - Share on GitHub with clean commits, readable documentation, and practice using issues for tracking.

---

### Tips for Success:
✅ Use **VS Code GitLens** for visualization.  
✅ Pair this schedule with **daily notes** on what you learned.  
✅ Actively commit code on GitHub to build a **public practice portfolio**.

If you would like, I can also generate **ready practice commands, test repos, and a capstone project idea** to match this plan for your daily execution. Let me know!

