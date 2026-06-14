STEP 1 Command
Bash

uname -r && pacman -Q | grep -E "linux|headers"

STEP 2 Command
Bash

lspci -k | grep -A 3 -E "VGA|3D"

STEP 3 Command
Bash

nvidia-smi

STEP 4 Command
``Bash

env | grep -E "XDG_SESSION_TYPE|WAYLAND"``

STEP 5 Command
``Bash

prime-run glxinfo | grep "OpenGL renderer"``
