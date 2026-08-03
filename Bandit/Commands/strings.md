## 🎯 1. Purpose

```
Extract readable text (ASCII characters) from binary files
```

---

## ⚙️ 2. Syntax

```
strings [filename]
```

---

## 🔹 3. Basic Usage

### Extract readable text from a file

```
strings data.txt
```

Output:

```
Shows human-readable parts inside the file
```

---

## 🧠 4. When to Use

```
Use strings when:
- cat output is unreadable
- file contains binary data
- you need to find hidden readable information
```

---

## 🔍 5. Practical Example

```
strings data.txt | grep "="
```

Breakdown:

```
strings data.txt
→ extracts readable strings

|
→ sends output to next command

grep "="
→ searches lines containing =
```

---

## ⚡ 6. Key Points

```
strings does not modify the file
It only displays readable characters
Useful for analyzing binary files
```

---

## 🧾 7. Commands Used

```
strings data.txt
strings data.txt | grep "="
```