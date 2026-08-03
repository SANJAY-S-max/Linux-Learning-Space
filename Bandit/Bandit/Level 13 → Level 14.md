# 🎯 Level Goal

```
Login as bandit14 using a private SSH key
→ then read /etc/bandit_pass/bandit14
```

---

# 🧠 Core Concept

```
This level introduces SSH key-based authentication

Instead of:
→ password login

You use:
→ private key file
```

---

# 🔐 What You Are Given

```
File: sshkey.private
```

👉 This is:

```
A PRIVATE SSH KEY (identity proof)
```

---

# ⚠️ CRITICAL RULE (MOST IMPORTANT)

```
❌ Do NOT SSH from inside bandit server
✅ Use your LOCAL machine
```

---

# 🧭 COMPLETE PROCEDURE

---

# 🔹 Step 1 — Login to bandit13

```
ssh bandit13@bandit.labs.overthewire.org -p 2220
```

👉 Enter password (from previous level)

---

# 🔹 Step 2 — Transfer Key to Local Machine

👉 Run on **your machine terminal (not inside bandit)**

```
scp -P 2220 bandit13@bandit.labs.overthewire.org:~/sshkey.private .
```

---

## 🧠 What `scp` does

```
Securely copies file over SSH
```

---

## 🔍 Syntax

```
scp -P <port> <user>@<host>:<remote_path> <local_path>
```

---

# 🔹 Step 3 — Fix Key Permissions

```
chmod 600 sshkey.private
```

---

## 🧠 Why this matters

```
SSH enforces strict permissions on private keys
```

---

## 🔍 Permission Breakdown

|Mode|Meaning|
|---|---|
|600|owner read/write only|

```
-rw-------
```

---

# 🔹 Step 4 — Login Using Private Key

```
ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220
```

---

## 🔍 Command Breakdown

|Part|Meaning|
|---|---|
|`ssh`|secure login|
|`-i`|identity file (private key)|
|`bandit14`|target user|
|`-p 2220`|custom port|

---

# 🔹 Step 5 — Verify Identity

```
whoami
```

Expected:

```
bandit14
```

---

# 🔹 Step 6 — Retrieve Password

```
cat /etc/bandit_pass/bandit14
```

👉 🎉 This is your next level password

---

# 🧠 How SSH Key Authentication Works

---

## 🔐 Concept

```
Private Key (you have) ↔ Public Key (server has)
```

---

## 🔄 Flow

```
1. Client sends request
2. Server checks public key
3. Client proves identity using private key
4. Access granted (no password needed)
```

---

## 🔥 Key Insight

```
Private key = your identity
If leaked → full access
```

---

# ⚠️ Common Errors & Fixes

---

## ❌ Error: Permission denied (chmod failed)

```
Cause: trying inside bandit server
```

✔ Fix:

```
Do chmod on your local machine
```

---

## ❌ Error: UNPROTECTED PRIVATE KEY FILE

```
Permissions too open
```

✔ Fix:

```
chmod 600 sshkey.private
```

---

## ❌ Error: Connecting from localhost is blocked

```
You tried SSH inside bandit
```

✔ Fix:

```
Run SSH from your system
```

---

## ❌ Error: Permission denied (publickey)

✔ Causes:

```
- Wrong key
- Wrong permissions
- Wrong user
```

---

# 🔁 Execution Flow (Compact)

```
# LOCAL MACHINE

ssh bandit13@bandit.labs.overthewire.org -p 2220

scp -P 2220 bandit13@bandit.labs.overthewire.org:~/sshkey.private .

chmod 600 sshkey.private

ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220

cat /etc/bandit_pass/bandit14
```

---

# 🧰 Commands Used (Quick Reference)

|Command|Purpose|
|---|---|
|`ssh`|remote login|
|`scp`|file transfer|
|`chmod`|change permissions|
|`cat`|read file|
|`whoami`|confirm user|

---

# 🔐 Security Concepts Learned

---

## 🔹 Authentication Types

|Type|Example|
|---|---|
|Password|bandit login|
|Key-based|this level|

---

## 🔹 Principle

```
Least privilege + secure credentials
```

---

## 🔹 Why strict permissions?

```
Prevent others from reading your private key
```

---

# 🏁 Final Insight

```
This level is about:

→ Understanding SSH key authentication
→ Handling secure credentials
→ Knowing where to execute commands (local vs remote)
```

---

# ✅ What You Mastered

```
✔ SSH key login
✔ SCP file transfer
✔ Permission model (chmod 600)
✔ Remote access control
```