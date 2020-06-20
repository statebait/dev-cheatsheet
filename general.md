# General Commands

General commands for linux/shell/bash etc.

### 1. To move files (and folders) (can be used to rename files/folders):

```bash
mv <current_file_path> <new_file_path>
```

### 2. Delete a folder with files in it:

```bash
rm <folder_path> -rf
```

### 3. To list files and folders inside present working directory:

- Basic use:

  ```bash
  ls
  ```

- List hidden folders too:

  ```bash
  ls -a
  ```

### 4. To get the path of the present working directory:

```bash
pwd
```

### 5. Compress/Extract a folder using tar:

- Compress:

  ```bash
  tar -zcvf <file_name>.gz <folder_name>
  ```

* Extract:

  ```bash
  tar -xf <file_name>.gz
  ```

### 6. Send a file using SCP to a remote server:

```bash
scp <file_name> <user>@<server_ip>:/remote/folder/
```
