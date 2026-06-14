# 🗺️ Linux Basics for Hackers
> **Note:** A curated collection of essential commands.
---

## 📖 Chapter 1: Recon & Navigation

### 🔍 Identifying the System
Before executing payloads or scripts, figure out who you are and what machine you're standing on:
```bash
whoami      # Prints current logged-in user
uname -a    # Prints kernel version and system architecture
hostname    # Prints the network name of the machine

```

### 🐚 Enumerating the Shell

Find out which shell environment you are trapped in:

```bash
echo $SHELL # Prints the path to the default shell
echo $0     # Prints the name of the currently running process/shell
ps          # Lists active processes in the current session

```

### 🚗 Moving Around the Filesystem

```bash
.           # Represents the CURRENT directory
..          # Represents the PARENT directory (one level up)
cd ../..    # Jump up two directory levels at once

```

### 💔 Getting Help

When you don't know how a tool works, check the manual or help flags:

```bash
man command       # Open the official system manual page
command --help    # Common flag for detailed tool help
command -h        # Short form help flag

```

### 🔎 Finding Stuff

Locating hidden configuration files, target scripts, or specific binaries:

```bash
locate fileName                              # Fast database search for files
sudo updatedb                                # Fixes "Short read/corrupted" database errors
which filename                               # Shows the absolute path of an executable binary
find . -type f -name "fileName*" 2>/dev/null # Deep search, hiding permission errors

```

---

## 📖 Chapter 2: Text Manipulation


### 😲 Inspecting and Filtering Files

```bash
nl /etc/passwd                        # View a file with line numbers attached
grep "noob" /etc/passwd               # Search and extract lines containing a specific keyword
tail -n+10 /etc/passwd | head -n 3    # Slices the file to print exactly lines 10-12
history | grep "snapper"              # Search your past commands for specific keywords

```
### ✈️ Inside less or man:

```Bash
/keyword    # Search forward for a word
?keyword    # Search backward for a word
n / N       # Next match / Previous (Last) match

```
## 📖 Chapter 3: Networking

### 🐶 Inspecting the Network

```bash
ip a                                  # View all active IP and MAC addresses (Replaces ifconfig)
ip r                                  # Check your routing table and default gateway

```
