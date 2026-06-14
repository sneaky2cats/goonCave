START

### STEP 1: Core & Blueprint Verification (The Kernel & Headers)

**Command:**

```bash
uname -r && pacman -Q | grep -E "linux|headers"
```

**Logic:**
Software cannot talk to hardware without a bridge. Ensure the running kernel matches the active header version exactly.

---

### STEP 2: Hardware Awareness (The Detection)

**Command:**

```bash
lspci -k | grep -A 3 -E "VGA|3D"
```

**Logic:**
Confirm the motherboard physically sees both chips (Intel/AMD + NVIDIA) and verify that the **Kernel driver in use** is `nvidia`, not `nouveau` (open-source) or `none`.

---

### STEP 3: Driver State (The Pulse Check)

**Command:**

```bash
nvidia-smi
```

**Logic:**
Query the NVIDIA binary directly. If it responds, the driver is alive. Check **Processes**—if empty on a hybrid laptop, the card is successfully idling (saving power).

---

### STEP 4: Display Server Environment (The Context)

**Command:**

```bash
env | grep -E "XDG_SESSION_TYPE|WAYLAND"
```

**Logic:**
Identify if the system runs X11 or Wayland. Wayland handles multi-GPU routing automatically; X11 requires manual provider mapping.

---

### STEP 5: Render Offload Test (The Execution)

**Command:**

```bash
prime-run glxinfo | grep "OpenGL renderer"
```

**Logic:**
Force a specific application onto the discrete GPU. If the output string names the NVIDIA card instead of the integrated GPU, PRIME is active.

---

**Logic:**
Forcing ACPI sleep states tests whether the driver can gracefully save its VRAM state to system RAM and re-initialize GPU hardware clocks upon wake without panicking.

END
