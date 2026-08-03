## 🎯 1. Goal

```
Find a file that:
- is owned by user bandit7
- is owned by group bandit6
- is exactly 33 bytes in size
```

---

## 📁 2. Directory Situation

```
Home directory has no useful files
→ Need to search entire system
```

---

## 🧠 3. Core Concept: Advanced find Filters

```
Use find with:
-user  → filter by owner
-group → filter by group
-size  → filter by file size
```

---

## 🔍 4. Key Technique

```
find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null
```

---

## ⚠️ 5. Error Handling

```
Searching from / gives many permission errors
```

Solution:

```
2>/dev/null
```

```
2 → error output
/dev/null → discard errors
```

---

## 🔹 6. Output Handling

```
Command returns file path
```

Example:

```
/path/to/file
```

Read it:

```
cat /path/to/file
```

---

## ⚙️ 7. Commands Used

```
find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null
cat /path/to/file
```

---

## 🧾 Summary

```
Use find with user, group, and size filters across /, then cat the result
```

