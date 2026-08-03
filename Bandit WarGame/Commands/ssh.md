## ✅ Definition

**SSH (Secure Shell)** is a way to **connect to another computer remotely** and control it using the command line.

## 🧠 Simple Analogy

Think of SSH like:

> 📱 _Using your phone to control another computer far away securely_

---

## ⚙️ How it works

You type:

```
ssh username@server_ip
```

Example:

```
ssh user@192.168.1.10
```

### What happens:

1. Your computer connects to another system (server)
2. You log in (password or key)
3. You get a terminal of that remote machine
4. Now you're controlling it as if you're sitting there
## 🔐 Why “Secure”?

- Data is **encrypted**
- No one can easily intercept your commands

---
## 🔧 Syntax 

```shell
bash ssh username@host -p port
```

## 🔹 With private key

```
ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220
```

## 🧪 Real-world usage

- Managing cloud servers (AWS, Azure)
- Working on college/company servers
- Running programs remotely

## 🔍 Breakdown

| Part        | Meaning                |
| ----------- | ---------------------- |
| `ssh`       | secure shell           |
| `user@host` | target login           |
| `-p 2220`   | custom port            |
| `-i file`   | identity (private key) |

## 🧠 Behavior

```
- Encrypts connection
- Authenticates user
- Opens remote shell
```
## Link
[[Bandit Level 0]]
