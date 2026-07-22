---
category: Hardware
---


>[!info] lshw (List Hardware) 
>command** in Linux is a powerful command-line utility used to extract **detailed information about the system's hardware configuration.
``` bash
pacman -S lshw
```

>[!quote] It reads raw details from various system files (like the `/proc` directory and `sysfs`), combines it with DMI data, and generates a structured profile of your computer's internal architecture. 
``` bash
sudo lshw -short
sudo lshw -html > hwinfo.html
```
>[!tip]- [[Options lshw]]
![[Options lshw]]

---

>[!info] lspci (List PCI) 
>is a Linux command-line utility used to display detailed information about all **PCI (Peripheral Component Interconnect)** buses and the devices connected to them. It helps identify internal hardware like graphics cards, network adapters, USB controllers, and storage devices.

---

>[!info] lscpu 
>command in Linux is a utility that displays detailed information about your system's CPU architecture. It gathers and aggregates hardware data to show the number of CPUs, cores, threads, sockets, NUMA nodes, as well as cache configurations, vendor ID, and CPU family. 

---

>[!info] lsblk 
>command (short for **"list block devices"**) is a built-in utility used to **display information about all available storage devices** (like hard drives, SSDs, flash drives, and partitions) in a Linux system. It reads the `sysfs` filesystem and `udev` database to gather and display data in a clean, tree-like layout.
``` bash
lsblk -f
lsblk -d
```

---

>[!info] lsusb
> (short for **list USB**) is a command-line utility in Linux that displays detailed information about all USB buses and the devices connected to them. It reveals hardware specs like vendor IDs, product IDs, and the physical connection hierarchy
``` bash
sudo pacman -S usbutils
```

---
>[!info] Dmidecode
> is a command-line utility that decodes a computer's DMI (Desktop Management Interface) table into human-readable text. It extracts deep hardware information straight from your BIOS/UEFI, including system manufacturer, serial numbers, exact BIOS version, and precise RAM/CPU specifications, without probing the hardware directly
``` bash
sudo dmidecode | grep -A3 '^System Information'
```
>[!tip]- [[dmidecode_options]]
>![[dmidecode_options]]


