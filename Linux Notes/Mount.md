

>[!info] Mount NTFS
```
sudo mkdir /mnt/ntfs
sudo mount -t ntfs-3g /dev/sdb1 /mnt/ntfs -o uid=1000,gid=1000  
```

>[!info] Mount VFAT
```
sudo mount -t vfat /dev/sdb1 /mnt/usb -o rw,uid=$(id -u),gid=$(id -g)
```

>[!info] Mount windows share folder over lan

``` bash 
$ sudo mount -t cifs //192.168.18.3/amrk /mnt/amrk -o  username=kuvedi,password=matrix
```

