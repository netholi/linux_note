
>[!info] chmod
> Used to change the mode (permissions) of a file or directory.

>[!example] Ex:  (Adding/Removing)
>
``` bash
chmod g+w file3.txt
chmod o-r file3.txt 
```

>[!quote]  add execute to user, add write and execute to group and remove all permission for other - permission already assigned is untouched 
``` bash
 chmod u+x,g+rwx,o-rwx file3.txt    
```
>[!quote] ( =  sign reassign the permission to the exact mode , previous modes are overwritten)
``` bash
 chmod u=rwx,g=rw,o-rwx file3.txt  
```

``` bash
(Numerical): chmod 660 file4.txt 
```
 
>[!info] chown  
>Used to change the owner (and optionally the group) of a file or directory.
``` bash
sudo chown jdoe:marketing file1.txt 
```

>[!info] chgrp 
>Used specifically to change the group ownership of a file.
``` bash
 chgrp marketing file6.txt 
```

>[!important] Note on recursion: For commands like chmod, chown, and chgrp, you can use the -R (or -r) flag to apply changes recursively to a directory and all its sub-contents.
``` bash
 sudo chown -R dpazette ~/* 
```
