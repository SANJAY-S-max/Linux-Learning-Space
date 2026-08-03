## 🎯 1. Goal

```
Find the file that:
- is human-readable
- is exactly 1033 bytes in size
- is not executable
```

---

## 📁 2. Directory Structure

```
bandit5 home
└── inhere/
    ├── maybehere00/
    ├── maybehere01/
    ├── maybehere02/
    └── ...
```

- Many subdirectories
- Many files inside them

---

## 🧠 3. Core Concept: File Filtering

```
We don’t manually check files
→ Use find command to filter files
```

Conditions:

```
-readable
-size 1033 bytes
-not executable
```

---

## 🔍 4. Key Technique: Using find

### Command:

```
find . -type f -size 1033c
```

### Breakdown:

```
.          → current directory
-type f    → only files
-size 1033c → exactly 1033 bytes
```

---

## ⚠️ 5. Important Detail

After running `find`, you’ll get something like:

```
./maybehere07/.file2
```

Now read it:

```
cat ./maybehere07/.file2
```

---

## ⚙️ 6. Commands Used

```
cd inhere
ls
find . -type f -size 1033c
cat ./path/to/file
```
- [[find]]
---

## 🧾 Summary

```
Use find with size filter to locate the correct file, then cat to read it
```

---

## 🔥 Tip (Important for future levels)

```
find is one of the most powerful Linux commands
You will use it a LOT
```