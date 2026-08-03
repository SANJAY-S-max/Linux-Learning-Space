## 🎯 1. Purpose

```
Search for specific text (pattern) inside files
```

---

## ⚙️ 2. Syntax

```
grep [options] "pattern" [file]
```

- **pattern** → text to search
- **file** → file to search in

---

## 🔹 3. Basic Usage

### Search word in a file

```
grep "hello" file.txt
```

👉 Shows lines containing **hello**

---

### Case-insensitive search

```
grep -i "hello" file.txt
```

---

### Show line numbers

```
grep -n "hello" file.txt
```

---

### Search multiple files

```
grep "hello" file1 file2
```

---

## 🔍 4. Common Options

```
-i → ignore case
-n → show line numbers
-r → recursive search (folders)
-v → invert match (NOT matching lines)
```

---

## 🧠 5. Core Concept: Pattern Matching

```
grep searches line-by-line
Returns lines that match the pattern
```

Example:

```
grep "password" data.txt
```

---

## ⚡ 6. Practical Example (Bandit)

```
grep "millionth" data.txt
```

👉 Finds line containing the word **millionth**

---

## 🔁 7. Typical Workflow

```
ls
cat file.txt
grep "text" file.txt
```

---

## ⚙️ 8. Commands Used (Bandit Style)

```
grep "text" filename
```

---

## 🧾 One-Line Summary

```
grep searches for specific text inside files and shows matching lines
```