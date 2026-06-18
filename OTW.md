# 🧩 OverTheWire Bandit – Cheat Sheet ✨

---

## 🔓 OTW Passwords - Use these! 
```Bash
ssh -bandit* -p 2220 bandit.labs.overthewire.org
# bantit0 bandit0
# bandit1 ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If
# bandit2 263JGJPfgU6LtdEvgfWU1XP5yac29mFx
# bandit3 MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
# bandit4 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
# bandit5 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
# bandit6 HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
```

---

## 🚀 SSH Connection
```Bash
ssh -p <PORT> -l <USERNAME> <HOST>
# OR shorter way:
ssh <USERNAME>@<HOST> -p <PORT>
```
💡 Note: host = hostname — exactly the same thing!

---

❌ URLs ≠ Hostnames: https://.../path is NOT a host
✅ Hostname: Only the address part (no slashes, no paths)

---

## 🪄 Magic Commands We Love
```Bash
file <name>         # Detect what’s inside (text? garbage? binary?) 🧠
file ./-file*       # Works even if filename starts with "-" ! ⚠️
cat ./<filename>    # Use ./ to avoid mistakes with weird names ✅
cat * 2>/dev/null   # Read all files, hide errors silently 🤫
```
---

## ✅ THE ONLY COMMAND YOU NEED
```Bash
find . -type f -size 1033c ! -executable -exec cat {} +
```

---

## 📘 Breakdown (how to build it yourself):

```Bash
find .	        # Search EVERYTHING here (all folders, hidden files, dash files, spaces)
-type f	        # Only look for files (skip folders)
-size 1033c     # Exact size = 1033 bytes → c = BYTES (CRITICAL! without c it’s wrong)
! -executable   # ! = NOT → file has NO execute permission (-rw-r-----)
-exec cat {} +	# Automatically print the content of what we found
```
