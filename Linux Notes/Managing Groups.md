>[!quote] Info
The newgrp command is moved to new package
``` bash
sudo apt install util-linux-extra
```

>[!info] groups 
>Displays the groups a user belongs to.
>Example: groups [username] lists all groups for the specified user.

>[!info] groupadd
>Creates a new group.
``` bash
sudo groupadd sales 
```

>[!info] groupmod 
>Modifies an existing group, such as changing its name using the -n flag.
>change marketing to Marketing (capitlize the first char)
``` bash
sudo groupmod -n Marketing marketing 
```

>[!info] groupdel
> Deletes an existing group.
``` bash
 sudo groupdel marketing
```

>[!info] gpasswd 
>Used to manage group members. The -a flag adds a user, while -d removes one. Using -A makes a user an administrator of the group.

``` bash
 (Add): sudo gpasswd -a jdoe sales 
 
 (Delete): sudo gpasswd -d zach sales 
```

>[!info] getent 
>get information from admin database - list all users in a group
``` bash
getent group Marketing
```

>[!info] newgrp 
>Temporarily changes the current group context for a user session.
``` bash
 newgrp marketing 
```

>[!info] chgrp 
>Changes the group ownership of a file.
``` bash
 chgrp marketing file1.txt 
```
