## 🔹 Command

```
scp -P 2220 bandit13@bandit.labs.overthewire.org:~/sshkey.private .
```

---

## 🔹 Purpose

Securely copy file from remote → local

---

## 🔍 Syntax

```
scp -P <port> <user>@<host>:<remote_path> <local_path>
```

---

## 🔍 Breakdown

|Part|Meaning|
|---|---|
|`scp`|secure copy|
|`-P 2220`|SSH port|
|`user@host:`|remote system|
|`~/sshkey.private`|source file|
|`.`|current directory|

---

## 🧠 Behavior

```
- Uses SSH protocol
- Requires authentication
- Transfers file securely
```