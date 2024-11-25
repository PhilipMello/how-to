# WSL Commands:

## How to install Linux on Windows with WSL
[How to install Linux on Windows with WSL](https://learn.microsoft.com/en-us/windows/wsl/install)

### List your installed WSL version
```
wsl --list -v
```
OR
```
wsl -l -v
```

---
### List available online WSL version to install
```
wsl --list --online
```
OR 
```
wsl -l -o
```

---
### Install WSL Linux version
```
wsl --install -d <DistroName>
Example: wsl --install -d Ubuntu-22.04
```
OR use the command below to install default WSL version
```
wsl --install
```

---
### Remove WSL Linux Version
```
wsl --unregister Ubuntu-22.04
```

### Install diffent versions
```
wsl --import TAG-NAME OS-IMAGE-FILE.tar

Example: wsl --import  RockyLinux-9-Base RockyLinux-9-Base Rocky-9-Container-Base.latest.x86_64.tar
```

---
### Upgrade version from WSL 1 to WSL 2
The wsl --set-version command can be used to downgrade from WSL 2 to WSL 1 or to update previously installed Linux distributions from WSL 1 to WSL 2.
```
wsl --set-version
```

## Time issue on WSL
To fix time issue in WSL, Run:
- Install ntpdate
```
apt install ntpdate
```
- Run:
```
sudo ntpdate pool.ntp.org
```
