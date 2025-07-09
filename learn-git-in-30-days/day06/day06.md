# Day-06: Tasks

1. Git Branching - Remote Branches

## Remote branches

- Remote references are references (pointers) in your remote repositories, including branches, tags, and so on. You can get a full list of remote references explicitly with `git ls-remote <remote>`, or `git remote show <remote>` for remote branches as well as more information. Nevertheless, a more common way is to take advantage of remote-tracking branches.
- This may be a bit confusing, so let’s look at an example. Let’s say you have a Git server on your network at `git.ourcompany.com`. If you clone from this, Git’s clone command automatically names it `origin` for you, pulls down all its data, creates a pointer to where its master or main branch is, and names it `origin/master` locally. Git also gives you your own local master branch starting at the same place as origin’s master branch, so you have something to work from.

  > `Note`: "origin" is not special

  > Just like the branch name “master” does not have any special meaning in Git, neither does “origin”. While “master” is the default name for a starting branch when you run git init which is the only reason it’s widely used, “origin” is the default name for a remote when you run git clone. If you run git clone -o booyah instead, then you will have booyah/master as your default remote branch.

![Remote branch](./img/remote-branches-1.png)
![Remote branch](./img/remote-branches-2.png)
`Server and local repositories after cloning`

- To synchronize your work with a given remote, you run a `git fetch <remote>` command (in our case, `git fetch origin`). This command looks up which server “origin” is (in this case, it’s git.ourcompany.com), fetches any data from it that you don’t yet have, and updates your local database, moving your origin/master pointer to its new, more up-to-date position.
  ![Remote branch](./img/remote-branches-3.png)
  `git fetch updates your remote-tracking branches`

#### continue

https://git-scm.com/book/en/v2/Git-Branching-Remote-Branches
