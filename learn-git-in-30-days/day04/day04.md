# Day-04: Tasks

## 1. Git Branching - Basic Branching and Merging

---

## Basic Branching and Merging

- Let’s go through a simple example of branching and merging with a workflow that you might use in the real world. You’ll follow these steps:
  - Do some work on a website
  - Create a branch for a new user story you are working on
  - Do some work in that branch
- At this stage, you’ll receive a call that another issue is critical and you need a hotfix. You’ll do the following:
  - Switch to your production branch.
  - Create a branch to add the hotfix.
  - After it’s tested, merge the hotfix branch, and push to production.
  - Switch back to your original user story and continue working.

### Basic Branching

- First, let’s say you’re working on your project and have a couple of commits already on the master branch.
  ![basic Branch 1](./img/basic-branching-1.png)
  `A simple commit history`

---

- You’ve decided that you’re going to work on issue #53 in whatever issue-tracking system your company uses. To create a new branch and switch to it at the same time, you can run the `git checkout` command with the `-b` switch:
  ![create branch and switch using -b](./img/create-iss53-branch-and-switch.png)

  ***

  ![git branching 2](./img/basic-branching-2.png)
  `Creating a new branch pointer`

---

- The iss53 branch has moved forward with your work
- Now you get the call that there is an issue with the website, and you need to fix it immediately. With Git, you don’t have to deploy your fix along with the `iss53` changes you’ve made, and you don’t have to put a lot of effort into reverting those changes before you can work on applying your fix to what is in production. All you have to do is switch back to your `main` branch.

```bash
git checkout main
Switch to branch 'main'
```

- At this point, your project working directory is exactly the way it was before you started working on issue #53, and you can concentrate on your hotfix. This is an important point to remember: when you switch branches, Git resets your working directory to look like it did the last time you committed on that branch. It adds, removes, and modifies files automatically to make sure your working copy is what the branch looked like on your last commit to it.
- Next, you have a hotfix to make. Let’s create a `hotfix` branch on which to work until it’s completed:
  ![hotfix branch](./img/hotfix-branch.png)
  ![git branching 4](./img/basic-branching-4.png)
  `Hotfix branch based on master/main`

---

- You can run your tests, make sure the `hotfix` is what you want, and finally merge the hotfix branch back into your `master/main` branch to deploy to production. You do this with the `git merge` command:
  ![another commit from hotfix](./img/another-commit-from-hotfix.png)

```bash
git checkout main
git merge hotfix
```

![git merge](./img/git-merge.png)

---

- You’ll notice the phrase “fast-forward” in that merge. Because the commit `C4` pointed to by the branch `hotfix` you merged in was directly ahead of the commit `C2` you’re on, Git simply moves the pointer forward. To phrase that another way, when you try to merge one commit with a commit that can be reached by following the first commit’s history, Git simplifies things by moving the pointer forward because there is no divergent work to merge together — this is called a “fast-forward.”
- Your change is now in the snapshot of the commit pointed to by the master branch, and you can deploy the fix.
  ![git branching-5](./img/basic-branching-5.png)
  `master is fast-forwarded to hotfix`

---

- After your super-important fix is deployed, you’re ready to switch back to the work you were doing before you were interrupted. However, first you’ll delete the `hotfix` branch, because you no longer need it — the `master/main` branch points at the same place. You can delete it with the `-d` option to git branch:
  `Delete hotfix branch`

```bash
git branch -d hotfix
git branch -d testing
```

`O/P`

```bash
git branch -d hotfix
git branch -d testing
Deleted branch hotfix (was 8e8ccaf).
Deleted branch testing (was 25f37b6).
```

- Now you can switch back to your work-in-progress branch on issue #53 and continue working on it.
