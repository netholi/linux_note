
>[!Warning] Repair ext4 disk
``` bash
sudo e2fsck -y /dev/sdXN
```

>[!Info] Adjust brightness
``` bash
sudo apt install brightnessctl
brightnessctl set 30%
```

>[!info] nmap
>Scan for host
``` bash
sudo nmap -sn 192.168.18.0/24
```

>[!info] ARP scan
``` bash
sudo arp-scan --localnet
```
