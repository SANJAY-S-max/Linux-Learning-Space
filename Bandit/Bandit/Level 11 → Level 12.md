## 🎯 Level Goal

```
The password for the next level is stored in data.txt
The file content is encoded using ROT13
```

---

## 🔐 Concept: ROT13

### 📖 Definition

```
ROT13 (Rotate by 13) is a substitution cipher
Each letter is shifted forward by 13 positions
```

---

### 🔄 Alphabet Mapping

```
ABCDEFGHIJKLMNOPQRSTUVWXYZ
NOPQRSTUVWXYZABCDEFGHIJKLM
```

---

### 🔄 Example

```
hello → uryyb
uryyb → hello
```

---

### ⚡ Key Properties

```
ROT13 is symmetric (same operation encodes and decodes)
Only letters are affected (A–Z, a–z)
Numbers and symbols remain unchanged
```

---

## 🛠️ Command Used: tr

### 🎯 Purpose

```
Translate or substitute characters
```

---

### ⚙️ Syntax

```
tr 'set1' 'set2'
```

---

### 💡 ROT13 Command

```
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```

---

## 🔍 Command Breakdown

### 📌 Read File

```
cat data.txt
```

```
Displays file content
```

---

### 📌 Transform Characters

```
tr 'A-Za-z' 'N-ZA-Mn-za-m'
```

```
A-M → N-Z
N-Z → A-M
a-m → n-z
n-z → a-m
```

---

### 📌 Pipe Operator

```
| passes output of one command as input to another
```

---

## 🧠 Mental Model

```
Think of alphabet as circular rotation:

A → N
B → O
...
N → A
```

---

## ⚙️ Step-by-Step Logic

```
1. File contains encoded text
2. Encoding is ROT13
3. Apply character rotation using tr
4. Output reveals actual password
```

---

## ⚡ Important Notes

```
ROT13 does not require a key
Same command both encodes and decodes
tr works on standard input/output
```

---

## ❌ Common Mistakes

```
Forgetting quotes in tr command
Typing incorrect letter ranges
Not using pipe (|)
```

---

## 🧾 One-Line Summary

```
Use tr with ROT13 mapping to decode data.txt and retrieve the password
```