# Git Commands

### 1. To stop tracking a file (which is present in .gitignore):

```bash
git rm --cached <file>
```

### 2. Keeping a fork upto date:

- Add remote from original repository in your forked repository:

  ```bash
  cd into/cloned/fork-repo
  # remote name can be anything you want
  git remote add <remote_name> git://github.com/ORIGINAL-DEV-USERNAME/REPO-YOU-FORKED-FROM.git
  git fetch <remote_name>
  ```

- Updating your fork from original repo to keep up with their changes:

  ```bash
  # for branch master (you can change this for any branch)
  git pull <remote_name> master
  ```

- To update the remote fork on GitHub (or any other git hosting site):

  ```bash
  # this assumes that the remote forks name is origin (which is usually the case)
  # branch name can be changed up to your liking
  git push origin master
  ```

### 3. Amending a staged changed to a previous commit:

```bash
(some_branch) git commit --amend
```

### 4. Deleting tags (locally and remotely):

- Delete local tag:

  ```bash
  git tag -d <tag>
  ```

- Delete remote tag (for eg. on GitHub)

  ```bash
  git push --delete origin <tag>
  ```

### 5. Resetting a repo to a certain commit along with a remote

```bash
 git reset --hard <commit>
 git push -f <remote_name> master
```
