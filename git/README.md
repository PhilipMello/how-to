# HOW-TO GIT

### Create a new repository on the command line (Windows, Mac, Linux)

```
mkdir your-folder-name
example: mkdir my-git-course
```

### Create a new file on the command line (Windows, Mac, Linux)

```
echo "text-inseted-into-file" >> README.md
echo "text-inseted-into-file" >> TEXT.txt
echo "text-inseted-into-file" >> index.html
```

### Checking if it is a git project or the Status

```
git status
```

### Initialize the local directory as a Git repository

```
git init
```

### Add files

#### 1 file

```
git add file.txt
```

#### All files

```
git add .
```

### Commit

```
git commit -m "first commit"
```

### Check Git Branch

```
git branch
```

### List all Branches

```
git branch -a
```

### List Remote Branch

```
git branch -r
```

### Switch Branch

```
git checkout <existing_branch>
```

### Adding New Branch

```
git checkout -b <new_branch>
```

### Switch to Main Branch

```
git branch -M main
```

### Clone Git Repository

```
git clone https://github.com/PhilipMello/how-to-philipmello.github.io.git
```

### Add remote Origin

```
git remote add origin https://github.com/PhilipMello/how-to-philipmello.github.io.git
```

### Send to GitHub (Push)

```
git push
```

### Send to diffent Branch

```
git push -u origin another-branch
```