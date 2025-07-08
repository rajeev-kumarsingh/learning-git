# Basic Collaboration Concepts

## Practice: Use a Dummy Project to Simulate Feature Branch Workflows

This guide will walk you through the basic concepts of collaboration using Git and GitHub (or any Git-based platform) with a focus on **feature branch workflows**. It includes steps for setting up a dummy project, collaborating using branches, and simulating a pull request process.

---

## Objectives

- Understand Git feature branching.
- Simulate collaborative work on a dummy project.
- Learn how to create, switch, merge, and manage branches.
- Practice resolving merge conflicts.

---

## Prerequisites

- Git installed
- GitHub account or access to a Git server
- Basic understanding of Git commands

---

## Step-by-Step Guide

### 1. Set Up a Dummy Project

```bash
mkdir dummy-project
cd dummy-project
git init
```

Create a basic `README.md` file:

```bash
echo "# Dummy Project" > README.md
git add README.md
git commit -m "Initial commit with README"
```

Create a remote repository on GitHub and connect:

```bash
git remote add origin https://github.com/yourusername/dummy-project.git
git push -u origin main
```

---

### 2. Create a Feature Branch

```bash
git checkout -b feature-1
```

Make some changes, e.g., create a new file:

```bash
echo "print('Hello from Feature 1')" > feature1.py
git add feature1.py
git commit -m "Add Feature 1 script"
git push origin feature-1
```

---

### 3. Simulate Collaboration

Simulate another contributor creating a different branch:

```bash
git checkout main
git pull origin main
git checkout -b feature-2
echo "print('Hello from Feature 2')" > feature2.py
git add feature2.py
git commit -m "Add Feature 2 script"
git push origin feature-2
```

---

### 4. Create a Pull Request (PR)

- Go to GitHub repository.
- Open a PR from `feature-1` to `main`.
- Open another PR from `feature-2` to `main`.
- Review and approve.
- Merge PRs using GitHub interface.

---

### 5. Pull the Latest Changes

After PRs are merged:

```bash
git checkout main
git pull origin main
```

---

### 6. Simulate Merge Conflict (Optional)

Create a conflicting change in both `feature-3` and `main`:

```bash
git checkout -b feature-3
echo "print('Conflicting change')" > conflict.py
git add conflict.py
git commit -m "Add conflicting change from feature-3"
git push origin feature-3
```

In `main`, add a different version of the same file and push.

Try merging feature-3 into main; Git will prompt you to resolve the conflict manually.

---

## Conclusion

This exercise helps you:

- Understand collaborative workflows
- Use feature branches effectively
- Simulate real-world Git collaboration

---

## Tips

- Always pull the latest changes from `main` before creating a new branch.
- Keep feature branches small and focused.
- Use meaningful commit messages.
- Resolve conflicts early.

---

Happy Collaborating! 🚀

