# 🎯 Objective

```
data.txt (hexdump)
→ convert to binary
→ detect compression layers
→ extract/decompress repeatedly
→ reach ASCII password
```

---

# 🧠 Core Idea

```
This level = multi-layer encoding pipeline

Hexdump → Binary → (tar/gzip/bzip2 repeated) → Final Text
```

---

# ⚙️ Phase 1 — Initial Setup

## 🔹 Create Workspace

```
mktemp -d
cd /tmp/<random-folder>
```

---

## 🔹 Copy Input File

```
cp ~/data.txt .
```

---

## 🔹 Convert Hexdump → Binary

```
xxd -r data.txt > data
```

👉 Now:

```
file data
```

---

# 🔁 Phase 2 — Core Loop (IMPORTANT)

```
REPEAT:
file data
→ identify type
→ rename accordingly
→ extract/decompress
```

---

# 📦 FILE TYPES YOU USED (REAL LEVEL FLOW)

---

# 🟣 1. POSIX TAR ARCHIVE

```
file data
→ POSIX tar archive (GNU)
```

## 🧠 Meaning

```
Archive format (not compression)
Contains one or more files
```

## 🔧 Commands

```
mv data data.tar
tar -xf data.tar
ls
```

## 🔁 Then:

```
mv dataX.bin data
```

---

## 🔍 Extra (Important)

### List contents without extracting

```
tar -tf data.tar
```

---

## ⚠️ Key Behavior

```
- tar DOES NOT compress
- tar DOES NOT delete original
- extracts new file(s)
```

---

# 🔴 2. GZIP

```
file data
→ gzip compressed data
```

## 🧠 Meaning

```
Single-file compression
Fast, common
```

## 🔧 Commands

```
mv data data.gz
gunzip data.gz
```

---

## Alternative:

```
gzip -d data.gz
```

---

# 🔵 3. BZIP2

```
file data
→ bzip2 compressed data
```

## 🧠 Meaning

```
Better compression than gzip
Slower
```

## 🔧 Commands

```
mv data data.bz2
bunzip2 data.bz2
```

---

## Alternative:

```
bzip2 -d data.bz2
```

---

# ⚫ 4. RAW BINARY (.bin)

```
data5.bin, data6.bin, data8.bin
```

## 🧠 Meaning

```
Generic binary file
May contain:
- tar
- gzip
- bzip2
```

## 🔧 Action

```
file dataX.bin
mv dataX.bin data
```

---

# 🟢 5. FINAL ASCII TEXT

```
file data
→ ASCII text
```

## 🔧 Command

```
cat data
```

👉 🎉 Password revealed

---

# 🧰 ALL COMMANDS YOU USED (MASTER LIST)

---

## 🔹 `file` (MOST IMPORTANT)

```
file data
```

```
Detects actual file type (not based on extension)
```

---

## 🔹 `xxd`

```
xxd -r data.txt > data
```

```
Reverse hexdump → binary file
```

---

## 🔹 `tar`

```
tar -xf file
```

```
Extract archive
```

```
tar -tf file
```

```
List contents
```

---

## 🔹 `gzip / gunzip`

```
gunzip file.gz
```

```
Decompress gzip file
```

---

## 🔹 `bzip2 / bunzip2`

```
bunzip2 file.bz2
```

```
Decompress bzip2 file
```

---

## 🔹 `mv`

```
mv old new
```

```
Rename file (critical for workflow)
```

---

## 🔹 `ls`

```
ls
```

```
Check new extracted files
```

---

## 🔹 `cp`

```
cp ~/data.txt .
```

```
Copy file
```

---

## 🔹 `rm`

```
rm data
```

```
Remove conflicting file
```

---

## 🔹 `mktemp`

```
mktemp -d
```

```
Create secure temporary directory
```

---

# 🔁 COMPLETE EXECUTION FLOW

```
1. xxd -r data.txt > data

LOOP:
    file data

    IF tar:
        tar -xf data
        ls
        mv <new_file> data

    IF gzip:
        mv data data.gz
        gunzip data.gz

    IF bzip2:
        mv data data.bz2
        bunzip2 data.bz2

    IF ASCII:
        cat data → DONE
```

---

# ⚠️ CRITICAL RULES (EXAM LEVEL)

---

## ❗ Rule 1: Never trust filename

```
.bin, .txt, etc → meaningless
ONLY trust `file`
```

---

## ❗ Rule 2: Always normalize to `data`

```
mv dataX.bin data
```

---

## ❗ Rule 3: Ignore data.txt after conversion

```
Only used once (xxd step)
```

---

## ❗ Rule 4: Handle overwrite errors

```
rm data
```

OR

```
bunzip2 -f data.bz2
```

---

# 🧠 DEEP UNDERSTANDING

---

## 🔍 Compression vs Archive

|Type|Role|
|---|---|
|tar|archive (bundle files)|
|gzip|compression|
|bzip2|compression|

---

## 🔥 Key Insight

```
.tar → container
.gz / .bz2 → shrink data
```

---

## 🧠 Real Flow Example

```
data.txt
↓
binary
↓
tar
↓
gzip
↓
bzip2
↓
tar
↓
...
↓
ASCII
```

---

# 🏁 End Condition

```
file data
→ ASCII text
```

```
cat data
```

---

# 🚀 Final Master Insight

```
This level is NOT about commands

It is about:
→ recognizing file signatures
→ applying correct tool
→ maintaining clean workflow
```

---

# ✅ What You Mastered

```
✔ file type detection
✔ tar archive handling (POSIX tar)
✔ gzip & bzip2 decompression
✔ hexdump reversal (xxd)
✔ disciplined iterative workflow
```