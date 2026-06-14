QEMUKVM

```BASH
sudo pacman -S qemu-full virt-manager virt-viewer dnsmasq vde2 openbsd-netcat iptables-nft swtpm libvirt
```

qemu-full — the virtualization engine and device emulation.

virt-manager — graphical VM manager.

virt-viewer — viewer for SPICE/QEMU consoles.

libvirt — management layer used by Virt-Manager.

dnsmasq — networking for NATed VMs.

iptables-nft — firewall backend used by libvirt networking.

swtpm — software TPM (useful for Windows 11).

vde2 and openbsd-netcat — networking utilities often recommended with libvirt.
