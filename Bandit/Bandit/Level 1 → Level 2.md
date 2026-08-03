## 🎯 Goal
Find the password stored in a file named "-" in the home directory

## 🧪 Steps I Did
```bash
ls
cat ./-
```

## 💡 Explanation

- Used `ls` to list files and found a file named "-"
- Directly using `cat -` does not work as expected because "-" is treated as standard input
- Used `cat ./-` to explicitly specify the file in the current directory
- The output is the password for the next level

## 🧠 Key Takeaways

- "-" is treated as standard input in Linux commands
- Prefixing with `./` forces it to be treated as a filename
- Always use explicit paths for special filenames

## 🔥 Core Trick

- Using `./` to handle special filenames like "-"


---

# ✅ What You Just Learned (Important)

This is your first real Linux rule:
> **Not everything that looks like a filename is treated as a filename**

You must sometimes **force interpretation using paths (`./`)**

---


