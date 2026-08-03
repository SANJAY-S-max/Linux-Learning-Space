## 🔹 Basic Command

```
nc localhost 30000
```

## 🔹 Purpose

Connect to TCP service running on port 30000

---

## 🔍 Breakdown

|Part|Meaning|
|---|---|
|`nc`|netcat tool|
|`localhost`|current machine|
|`30000`|target port|

---

## 🔹 Interactive Usage

```
nc localhost 30000
# paste password
# press Enter
```

---

## 🔹 One-Line (IMPORTANT)

```
cat /etc/bandit_pass/bandit14 | nc localhost 30000
```

---

## 🔍 Pipe `|` Concept

```
Left command output → Right command input
```

---

## 🔹 Useful Flags (Advanced)

```
nc -v localhost 30000
```

|Flag|Meaning|
|---|---|
|`-v`|verbose (show connection info)|

---

```
nc -l 30000
```

|Flag|Meaning|
|---|---|
|`-l`|listen mode (server mode)|

---

# ⚙️ 4. `telnet` — Alternative Tool

---

## 🔹 Command

```
telnet localhost 30000
```

## 🔹 Purpose

Connect to TCP port manually

---

## 🔍 Behavior

```
- Opens connection
- Accepts input
- Displays response
```

---

## ⚠️ Note

```
Deprecated tool (use nc instead)
```