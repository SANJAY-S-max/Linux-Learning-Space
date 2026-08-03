## 🎯 1. Goal

```
Find the password in data.txt
The password is the only line that appears once
```

---

## 📁 2. Directory Situation

```
Home directory contains:
data.txt (many repeated lines)
```

- Most lines are duplicated
- Only one line is unique

---

## 🧠 3. Core Concept: Sorting & Uniqueness

```
Identify unique line using sorting and filtering
```

Tools:

```
sort → arrange lines
uniq → filter duplicates
```

---

## 🔍 4. Key Technique

```
sort data.txt | uniq -u
```

---

## 🔎 5. Command Breakdown

```
sort        → sorts all lines
|           → pipe (passes output)
uniq -u     → shows lines that appear only once
```

---

## ⚠️ 6. Important Concept

```
uniq works only on sorted input
```

---

## ⚙️ 7. Commands Used

```
sort data.txt | uniq -u
```

---

## ⚡ 8. Key Points

```
Use sort before uniq
-u → unique lines only
Pipe connects commands
```

---

## 🧾 Summary

```
Sort the file and use uniq -u to find the single unique line (password)
```
