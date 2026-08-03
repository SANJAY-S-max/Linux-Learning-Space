## 🎯 1. Purpose

```
Search for files and directories based on conditions
```

---

## ⚙️ 2. Syntax

```
find [path] [conditions]
```

- **path** → where to search
- **conditions** → filters (name, size, type, etc.)

---

## 🔹 3. Basic Usage

### Search all files in current directory

```
find .
```

---

### Search by name

```
find . -name "file.txt"
```

---

### Search only files

```
find . -type f
```

---

### Search only directories

```
find . -type d
```

---

## 🔍 4. Common Filters

### By size

```
find . -size 1033c
```

```
c → bytes
k → kilobytes
M → megabytes
```

---

### By readability

```
find . -readable
```

---

### Combine filters

```
find . -type f -size 1033c -readable
```

---

## ⚠️ 5. Important Points

```
. → current directory
find searches recursively (all subfolders)
Case-sensitive by default
```

---

## ⚡ 6. Practical Example (Bandit)

```
find . -type f -size 1033c
```

👉 Finds files that are:

- regular files
- exactly 1033 bytes

---

## 🔁 7. Typical Workflow

```
cd inhere
find . -type f -size 1033c
cat ./path/to/file
```

---

## 🧾 One-Line Summary

```
find searches files using conditions like name, size, and type
```