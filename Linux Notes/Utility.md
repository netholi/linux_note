
>[!important] Zoxide
>is a fast, Rust-based replacement for the traditional `cd` command that tracks your most frequently and recently used directories to let you "jump" to them instantly.
>
``` bash
sudo apt install zoxide
```
*Inside the ~/.bashrc add the following*
``` bash
eval "$(zoxide init bash)"
alias cd='z'
```

---

>[!important]  tealdeer  
>is an incredibly fast, community-driven, **Rust-based implementation of the `tldr` command. ** It bypasses long, wordy Linux `man` pages by providing **concise, practical, example-focused cheat sheets** right inside your terminal. 

>[!question] info
in case of error bad interpreter: No such file or directory arch Linux
``` bash 
sudo pacman -S python-pipx
pipx reinstall tldr
tldr -u
$tldr fd
```

---

>[!important]  sxhkd
is a lightweight, powerful **keyboard shortcut daemon for Linux** that executes commands in response to keypresses.
[[sxhkd configuration file]]

---

>[!important]  fzf
>a blazing-fast, general-purpose command-line interactive filter written in Go that significantly supercharges your Linux terminal workflow

---

>[!important]  bat   - batcat 
>feature-rich replacement for the traditional `cat` command, often described as a "cat clone with wings".

---

>[!important] fd 
>fast search  command

>[!info] *on archlinux the application is named fd*
```
pacman -S fd
```
 > [!info] *on debian based system*
```
apt Install fd-find  
```
> *(the command to use is fdfind)*
> *and alias it to fd="fdfind" in .bashrc*`

---
>[!important] wezterm terminal
>WezTerm is a powerful cross-platform terminal emulator and multiplexer. _Runs on Linux_, macOS, Windows 10, FreeBSD and NetBSD

---

>[!important] starship shell prompt  
![] (https://www.youtube.com/watch?v=v2S18Xf2PRo)
> <iframe width="421" height="240" src="https://www.youtube.com/embed/v2S18Xf2PRo" title="Ultimate Starship Shell Prompt Setup From Scratch" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

---

>[!important]  Stow 
>Manage dot files  
> [Youtube ] https://www.youtube.com/watch?v=06x3ZhwrrwA
> <iframe width="421" height="240" src="https://www.youtube.com/embed/06x3ZhwrrwA" title="How To Easily Manage Your Dotfiles With GNU Stow" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

``` bash
sudo apt install stow
```

---
>[!important] ripgrep
(invoked as `rg`) is a lightning-fast, line-oriented CLI search tool that recursively scans directories for regular expression patterns. Built in Rust, it serves as a highly performant, modern alternative to standard `grep`

---
>[!important]  rsync  
>**(Remote Sync) is a powerful, highly efficient command-line utility used in Linux for copying and synchronizing files and directories either locally or remotely across servers.** Unlike basic copy commands like `cp` or `scp`, `rsync` uses a unique delta-transfer algorithm. This ensures it only transmits the actual differences between the source and destination files, significantly saving time and network

>[!example] 
rsync --info=progress2 --remove-source-files *.webm  /mnt/media/malayalam/

---

>[!important] wormhole
>**Magic Wormhole** is a secure, command-line utility for Linux that allows you to easily transfer files, directories, or text snippets between two computers using short, human-readable codes.

- **Ubuntu / Debian / Kali Linux**: `sudo apt install magic-wormhole`
- **Arch Linux**: `sudo pacman -S magic-wormhole`
- **Fedora / RHEL**: `sudo dnf install magic-wormhole`
- **openSUSE**: `sudo zypper install python-magic-wormhole`
- **Universal Snap Package**: `sudo snap install wormhole`
   #distro-package-installer #installer #package-installer
>[!Example]
To send file
``` bash
wormhole send my_document.pdf
```
*you will receive a one-time phrase (e.g., `4-purple-dinosaur`). you need to send this pass-phrase to the receiver.*

To receive the file , type
``` bash
wormhole receive
```
*type the one-time phrase the sender sent you*

---
>[!important] yazi
>**is a blazing-fast, terminal-based file manager for Linux** written in Rust. It relies on non-blocking async I/O to load massive directories instantly without freezing the user interface.
---

---


>[!important] tmux
>is a powerful command-line tool in Linux. It allows you to run multiple terminal sessions inside a single window, split them into panes, and keep processes running in the background even if your SSH connection drops.

---

>[!important] transmission 
>is a powerful command-line tool in Linux. It allows you to run multiple terminal sessions inside a single window, split them into panes, and keep processes running in the background even if your SSH connection drops.

---

>[!important] tailscale
>Tailscale on Linux is a **zero-configuration VPN** powered by the **WireGuard** protocol that securely connects all your Linux devices, servers, and cloud instances into a private peer-to-peer mesh network. It assigns static private IP addresses to your machines and bypasses the need for open router ports or complex firewall rules.
[[Send files using tailscale]]

---

>[!important]  rustdesk
>is a secure, open-source remote desktop application that serves as a free alternative to TeamViewer and AnyDesk. Written in Rust, it allows users to remotely access and control Linux computers from Windows, macOS, iOS, Android, or the web.

---

>[!important] ncdu
>(NCurses Disk Usage) is a fast, interactive command-line tool for Linux and Unix systems that helps you analyze and free up disk space. It functions as a visual, text-based version of the standard `du` command, sorting files and folders by size within a navigable interface.

---

>[!important]  localsend
>is a free, open-source application that lets you securely share files and messages with nearby devices over your local Wi-Fi network, without requiring an internet connection.

---

>[!important]  fastfetch
>Fastfetch is a blazing-fast, highly configurable command-line tool that displays your system's hardware and software information in a neat, visually appealing layout== (complete with your operating system's logo). It serves as a modern, performance-oriented replacement for the discontinued _Neofetch_.

---
>[!important] Sipcalc 
> is a command-line IP subnet calculator that supports both IPv4 and IPv6. It provides detailed networking information—such as network ranges, broadcast addresses, and wildcard masks—and allows you to easily split networks based on smaller netmasks.
``` bash
sipcalc 192.168.18.15/24
```
---
