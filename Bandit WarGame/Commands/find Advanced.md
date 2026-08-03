## ⚙️ 1. Command: find (advanced usage)

### 🎯 Purpose

```
Search files with specific conditions (user, group, size)
```

---

### 🧾 Syntax Used

```
find / -type f -user bandit7 -group bandit6 -size 33c
```

---

### 🔍 Breakdown

```
/              → search from root (entire system)
-type f        → only files
-user bandit7  → file owner
-group bandit6 → file group
-size 33c      → file size = 33 bytes
```

---

## ⚙️ 2. Command: Error Redirection

### 🎯 Purpose

```
Hide permission errors while searching
```

---

### 🧾 Syntax

```
2>/dev/null
```

---

### 🔍 Meaning

```
2 → stderr (errors)
/dev/null → discard output
```

---

## ⚙️ 3. Command: cat

### 🎯 Purpose

```
Read file content (password)
```

---

### 🧾 Syntax

```
cat /path/to/file
```

---

## 🔁 4. Command Flow

```
find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null
cat /path/to/file
```

---

## ⚡ 5. Key Points

```
find can search entire system
Combine filters for precision
Use 2>/dev/null to suppress errors
Use cat to read result
```

---

## 🧾 One-Line Summary

```
Use find with filters and error redirection, then cat the result
```