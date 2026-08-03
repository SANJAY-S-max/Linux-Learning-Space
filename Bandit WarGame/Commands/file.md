# 📘 Command: file

## 🎯 Purpose

```
Identifies the type of a file (text, binary, image, etc.)
```

---

## ⚙️ Syntax

```
file [filename]
```

### Check all files in directory

```
file ./*
```

- `./*` → all files in current directory

## 🧠 Common Output Types

```
ASCII text        → readable text file
UTF-8 text        → readable text file (modern encoding)
data              → binary / unknown (not readable)
ELF executable    → program file
directory         → folder
```

