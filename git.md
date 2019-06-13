# Git Commands

### 1. To stop tracking a file (which is present in .gitignore):

```bash
git rm --cached <file>
```

### 2. Keeping a fork upto date:

- Add remote from original repository in your forked repository:

  ```bash
  cd into/cloned/fork-repo
  git remote add upstream git://github.com/ORIGINAL-DEV-USERNAME/REPO-YOU-FORKED-FROM.git
  git fetch upstream
  ```

- Updating your fork from original repo to keep up with their changes:

  ```bash
  git pull upstream master
  ```

- To update the remote fork on GitHub (or any other git hosting site):

  ```bash
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
