# 🧩 OverTheWire Bandit – Cheat Sheet ✨

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
