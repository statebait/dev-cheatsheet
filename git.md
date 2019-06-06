# Git Commands

### 1. To stop tracking a file (which is present in .gitignore):

```bash
git rm --cached <file>
```

### 2. Keeping a fork upto date:

- Clone your fork:

  ```bash
  git clone git@github.com:YOUR-USERNAME/YOUR-FORKED-REPO.git
  ```

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
