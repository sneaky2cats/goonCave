📖 ## Chapter 1
🔍 ### Identifying Stuff
```Bash
whoami
uname
hostname
```
🐚 ### Getting the Shell
```Bash
echo #SHELL
echo #0
ps
```
🚗 ### Moving Around
```Bash
.
..
cd ../..
```
💔 ### Getting Help
```Bash
help command
command --help
command -h
command -?
```
🔎 ### Finding Stuff
```Bash
locate fileName
updatedb
which filename
find -type file -name fileName.\* 2> /dev/null
```
😲 ### nl, grep, head, tail
```Bash
nl /etc/passwd
grep noob /etc/passwd
tail -n+10 /etc/passwd | head -n 3
history | grep snapper
```
## In less and man
```Bash
Summary Cheat Sheet
Tool	Search Mode	Go to Next	Go to Last (Previous)
less / man	/term	n	N
Terminal History	Ctrl + R	Ctrl + S	Ctrl + R
