# 🖥️ `ls` - List Directory Contents

## Description
The `ls` command is used to list the files and directories in a specified directory. By default, it displays the files in the current directory.

## Usage
```bash
ls [options] [path]
```

## Options

- **options**: Flags to modify the command's behavior (e.g., `-l`, `-a`, `-h`, etc.).
- **path**: The directory or file path to list. If no path is provided, it lists the current directory's contents.

## Common Options

- `-l`: Long format, shows file permissions, ownership, size, and modification date.
- `-a`: Includes hidden files (those starting with a dot).
- `-h`: Human-readable file sizes (with `-l`).
- `-R`: Recursively list subdirectories.
- `-t`: Sort files by modification time.
- `-S`: Sort files by size.

## Examples

## 1. Basic usage (current directory)
List the files in the current directory.

```bash
ls
```
## Example Output:
```bash
Desktop  Documents  Downloads  Music  Pictures  Videos
```

## 2. Long format listing
Display detailed information (permissions, ownership, size, and modification time).
```bash
ls -l
```
## Example Output:
```bash
drwxr-xr-x  2 user user 4096 Apr 25 12:34 Desktop
drwxr-xr-x  3 user user 4096 Apr 25 12:34 Documents
-rw-r--r--  1 user user    0 Apr 25 12:34 myfile.txt
```

## 3. Include hidden files
List all files, including hidden ones (files starting with a dot).
```bash
ls -a
```
## Example Output:
```bash
.  ..  .bashrc  .profile  Desktop  Documents  Downloads
```

## 4. Human-readable file sizes
List files with sizes in a human-readable format (e.g., KB, MB).
```bash
ls -lh
```
## Example Output:
```bash
-rw-r--r--  1 user user  2.0K Apr 25 12:34 myfile.txt
```

## 5. List files in a specific directory
List the files in a specific directory.
```bash
ls /home/user/Documents
```
## Example Output:
```bash
file1.txt  file2.txt  file3.pdf
```

## 7. Sort files by modification time
Sort files by the date they were last modified, with the newest files first.
```bash
ls -lt
```
## Example Output:
```bash
-rw-r--r--  1 user user  2.0K Apr 25 12:34 file3.txt
-rw-r--r--  1 user user  1.5K Apr 24 11:45 file2.txt
```
