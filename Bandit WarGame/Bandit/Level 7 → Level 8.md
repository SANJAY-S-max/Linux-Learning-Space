## 🎯 1. Goal

```
Find the password stored in data.txt
next to the word "millionth"
```

---

## 📁 2. Directory Situation

```
Home directory contains:
data.txt (large file with many lines)
```

- File is too large to read manually
- Need search-based approach

---

## 🧠 3. Core Concept: Text Searching

```
Search for a specific word inside a file
```

Target keyword:

```
millionth
```

---

## 🔍 4. Key Technique: grep

```
grep "millionth" data.txt
```

- Searches for lines containing **millionth**
- Outputs matching line

---

## 🔎 5. Output Handling

```
Result shows full line containing the word
Password is present in that line
```

Example:

```
xxxxxx millionth password_here
```

---

## ⚙️ 6. Commands Used

```
ls
grep "millionth" data.txt
```

---

## ⚡ 7. Key Points

```
grep is used for searching text
Works line-by-line
Best for large files
```

---

## 🧾 Summary

```
Use grep to find the line containing "millionth" and extract the password
```