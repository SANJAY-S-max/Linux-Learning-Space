## 🎯 1. Goal

```
Find the only human-readable file inside the inhere directory
```

---

## 📁 2. Directory Structure

```
bandit4 home
└── inhere/
    ├── -file00
    ├── -file01
    ├── -file02
    └── ...
```

- Many files
- Only ONE is useful

---

## 🧠 3. Core Concept: File Types

```
ASCII text → readable (contains password)
data → binary (not readable)
```

- Linux files are not all text
- Need to identify correct type

---

## 🔍 4. Key Technique: Identifying Correct File

```
Use file command to check type of all files
```

Example:

```
file ./*
```

- `./*` → all files in current directory
- Look for:

```
ASCII text
```

---

## ⚠️ 5. Special Case: Filenames Starting with -

```
Files starting with - are treated as options
```

Solution:

```
cat ./filename
```

Example:

```
cat ./-file02
```

---

## ⚙️ 6. Commands Used

```
cd inhere
ls
file ./*
cat ./<ASCII text file>
```

- [[file]]
- [[cat]]
---

## 🧾 Summary

```
Use file to find ASCII text file, then cat it using ./ to avoid option issues
```

