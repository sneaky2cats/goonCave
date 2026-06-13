# Linux Basics

## Checking Your Shell

### Commands to identify your shell:

```bash
echo $SHELL      # shows default/login shell
echo $0          # shows current shell
ps               # shows running processes
```

**Note:** Different shells have different features
- `bash` = traditional shell (has `help` built-in)
- `zsh` = modern shell (doesn't have `help` built-in by default)
- To run bash commands in zsh without switching: `bash -c "command"`

## User Information

```bash
whoami    # display current user (similar to: echo $USER)
```

## Process Management

```bash
ps              # list running processes in current terminal session
ps aux          # show ALL processes on the system (all users, detailed)
ps -ef          # similar to ps aux, different format
```

**Understanding ps output:**
- Shows all active processes
- By default, ps filters to just current shell/terminal activity
- `ps aux` shows everything running on the entire system
- When you run `ps`, you'll see the shell itself + the ps command you just ran

**Book Reference:** Linux Basics for Hackers - Chapter 1
