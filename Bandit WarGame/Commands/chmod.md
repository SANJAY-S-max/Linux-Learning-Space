## 🔹 Command

```
chmod 600 sshkey.private
```

---

## 🔹 Purpose

Set secure permissions on private key

---

## 🔍 Permission Meaning

|Mode|Access|
|---|---|
|6|read + write (owner)|
|0|no access (group)|
|0|no access (others)|

---

## 🔍 Result

```
-rw-------
```

---

## 🧠 Behavior

```
SSH refuses keys with loose permissions
```