
# [K9s Installation Guide for Ubuntu](https://k9scli.io/topics/install/)

K9s is a terminal-based UI that simplifies the management of Kubernetes clusters. This guide provides three methods to install K9s on Ubuntu:

- Using **Snap**
- Using a **Debian (.deb) package**
- Using a **direct binary download**

---

## 📦 1. Install K9s Using Snap

### Install Snap (if needed)
```bash
sudo apt update && sudo apt install snapd
```

### Install K9s via Snap
```bash
sudo snap install k9s
```

### Verify Installation
```bash
k9s version
```

---

## 📁 2. Install K9s Using a Debian Package

### Download the latest `.deb` package
```bash
wget https://github.com/derailed/k9s/releases/download/v0.32.5/k9s_linux_amd64.deb
```

### Install the package
```bash
sudo apt install ./k9s_linux_amd64.deb
```

### Remove the downloaded installer
```bash
rm k9s_linux_amd64.deb
```

### Verify Installation
```bash
k9s version
```

---

## 🔧 3. Install K9s via Direct Binary Download

### Create an installation directory
```bash
mkdir ~/k9s-installation && cd ~/k9s-installation
```

### Download the K9s binary
```bash
curl -LO https://github.com/derailed/k9s/releases/download/v0.32.4/k9s_Linux_amd64.tar.gz
```

### Extract the archive
```bash
tar xf k9s_Linux_amd64.tar.gz
```

### Move the binary into your PATH
```bash
sudo mv k9s /usr/local/bin
```

### Verify Installation
```bash
k9s version
```

---

## 🚀 Running K9s

Launch K9s using:
```bash
k9s
```

---

## 📚 Resources
- K9s GitHub Repository: https://github.com/derailed/k9s

