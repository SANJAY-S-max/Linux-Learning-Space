## 🎯 1. Goal

```
Find the password stored in data.txt

The password is:
- in a human-readable string
- preceded by several "=" characters
```

---

## 📁 2. File Situation

```
data.txt contains:
- binary data
- random characters
- some readable text
```

Normal reading:

```
cat data.txt
```

does not give useful output.

---

## 🧠 3. Core Concept: Extracting Strings

```
Binary files can contain readable text inside them

strings command extracts human-readable characters
from binary files
```

---

## 🔍 4. Key Technique

Extract readable content:

```
strings data.txt
```

Search for password pattern:

```
strings data.txt | grep "="
```

---

## 🔎 5. Command Breakdown

```
strings → extracts readable text from binary data

| → sends output from one command to another

grep "=" → searches lines containing =
```

---

## ⚠️ 6. Important Concept

```
Not every file is plain text

Some files contain:
- binary data
- hidden readable strings

Use strings when cat output is unreadable
```

---

## ⚙️ 7. Commands Used

```
ls
strings data.txt
strings data.txt | grep "="
```

---

## ⚡ 8. Key Points

```
strings helps inspect binary files
grep filters useful output
Pipe connects multiple commands together
```

---

## 🧾 Summary

```
Use strings to extract readable text from binary data,
then use grep to find the password pattern
```