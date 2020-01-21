# Git Commands

## Stash superpowers

> Great tutorial: https://www.atlassian.com/git/tutorials/saving-changes/git-stash

Knowing how to leverage `git stash` is a superpower and the following commands will allow you to do just that:

- Basic use (will store current changes to the stash):

```bash
git stash
```

- Save untracked files by:

```
git stash -u
```

- View(list) your stash:

```bash
git stash list
```

- Store a stash with a message:

```bash
git stash save "fire"
```

- Pop a stash(will pop the recent most stash):

```bash
git stash pop
```

- Pop a specific stash:

```bash
git stash pop <stash_id>
```

- Apply a stash without removing it(will apply the recent most stash):

```bash
git stash apply
```

- Apply a specific stash without removing it:

```bash
git stash apply <stash_id>
```

## Regular

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

### 3. Amending a staged changed to a previous commit or updating the commit message:

- Regular (will open selected editor for editing commit message):

  ```bash
  git commit --amend
  ```

- Editing the commit message directly:

  ```bash
  git commit --amend -m "<your new message>"
  ```

- Without editing commit message:

  ```bash
  git commit --amend --no-edit
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

### 5. Resetting a repo to a certain commit along with a remote:

```bash
 git reset --hard <commit>
 git push -f <remote_name> master
```

### 6. Viewing the current code diff:

```bash
git diff
```

### 7. Reverting changes done in a folder:

- If you have not yet indexed (git add) your changes:

  ```bash
  git checkout -- path/to/folder
  ```

- If changes are indexed then you need to reset that first:

  ```bash
  git reset -- path/to/folder
  git checkout -- path/to/folder
  ```

### 8. Updating the local list of remote branches:

```bash
git remote update origin --prune
```
