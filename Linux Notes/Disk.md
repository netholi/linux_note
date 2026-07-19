>[!Warning] Repair ext4 disk
``` bash
sudo e2fsck -y /dev/sdXN
```

>[!warning] Use this when Linux refuses to mount an NTFS drive because it reports an "unclean file system" or "dirty bit". 
``` bash
sudo ntfsfix --clear-dirty /dev/sdxx
```
