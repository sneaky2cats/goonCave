# 🗺️ Linux Basics for Hackers
> **Note:** A curated collection of essential commands.
---

## 📖 Chapter 1: Getting Started with the Basics

### 🔍 Identifying the System
Before executing payloads or scripts, figure out who you are and what machine you're standing on:
```bash
whoami    # Prints current logged-in user
uname -a  # Prints kernel version and system architecture
hostname  # Prints the network name of the machine

```

### 🐚 Enumerating the Shell

Find out which shell environment you are trapped in:

```bash
echo $SHELL  # Prints the path to the default shell
echo $0      # Prints the name of the currently running process/shell
ps           # Lists active processes in the current session

```

### 🚗 Moving Around the Filesystem

```bash
.         # Represents the CURRENT directory
..        # Represents the PARENT directory (one level up)
cd ../..  # Jump up two directory levels at once

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
locate fileName                               # Fast database search for files
sudo updatedb                                 # Fixes "Short read/corrupted" database errors
which filename                                # Shows the absolute path of an executable binary
find . -type f -name "fileName*" 2>/dev/null  # Deep search, hiding permission errors

```

## 📖 Chapter 2: Text Manipulation

### 😲 Inspecting and Filtering Files

```bash
nl /etc/passwd                      # View a file with line numbers attached
grep "noob" /etc/passwd             # Search and extract lines containing a specific keyword
tail -n+10 /etc/passwd | head -n 3  # Slices the file to print exactly lines 10-12
history | grep "snapper"            # Search your past commands for specific keywords

```
### ✈️ Inside less or man:

```Bash
/keyword    # Search forward for a word
?keyword    # Search backward for a word
n / N       # Next match / Previous (Last) match

```
## 📖 Chapter 3: Analyzing and Managing Networks

### 🐶 Inspecting the Network

```bash
xxx.xxx.xxx.xxx/yy                            # an IP address followed by a prefix length (subnet mask)
ip a                                          # View all active IP and MAC addresses (Replaces ifconfig)
ip r                                          # Check your routing table and default gateway
iw dev                                        # Lists wireless devices and their"phy"
```

### ⚔️ Replacing IP and Netmask

```bash
ip addr replace x.x.x.x/y dev z               # Assigns a new ip address and netmask
it addr replace x.x.x/y broadcat x.x.x dev z  # assigns a broadcast as well
```

### 🥷 Spoofing the Mac Address

```bash
ip link set dev z down                       # bring the interface down
ip link set dev z address XX:XX:XX:XX:XX:XX  # change mac address
ip link set dev z up                         # duh
```

### 🐕 Digging with dig

```bash
dig website.com  # defaults to addess record type
dig ns website.com          # name server record type
dig website.com mx          # mail server record type
dig txt website.com +short  # text reord type, shot version
dig @8.8.8.8 website.com    # specifies a dns resolver
```

### 🥊 hosts and resolv.conf are stored in:

```bash
/etc/resolv.conf
/etc/hosts
```

## Chapter 4: Adding and Removing Software

### 👾 Searching, Installing and Removing Packages in Arch

```bash

pacman -S package   # installs a packaage
pacman -Ss          # lists EVERY package in the repo
pacman -Ss package  # lists non installed matches
pacman -Q           # lists every installed package
pacman -Q package   # lists installed matches
pacman -Qs package  # lists matches
pacman -R package   # removes a package
pacman -Rs package  # removes a package and its dependencies
pacman -Rsn         # removes a package, it's dependencies and config files
```

---
