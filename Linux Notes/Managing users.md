>[!info] useradd 
>Creates a new user account.

>[!example] Ex
>Create a user JSmith, -c [comment] -e [expiry date]  -s [shell]
``` bash
sudo useradd -c "Jane Smith" -e 2019-12-31 -s /bin/csh JSmith 
```

>[!info]  id
> Displays information about a user, including their user ID (UID).
> Example: id Sarah

>[!info] userdel 
>Deletes a user account. The -r flag is recommended to remove the user's home directory.
``` bash
sudo userdel -r Sarah 
```
    
>[!info] usermod
> Modifies an existing user account.

>[!example] Example.   Add a comment to Sarah  / to rename the user 
``` bash
sudo usermod -c "Sarah Jones" 
sudo usermod -l SJones Sarah 
```

  >[!info] passwd 
  >Sets or updates a user's password.
``` bash
 sudo passwd SJones 
```

>[!info] chage 
>Changes user password expiration information and policies.
``` bash
chage -l SJones 
```

>[!info]  chsh 
>Changes a user's default login shell.

>[!tip] List the defaults
> list the defaults while creating the user like skel directory. 
> Look into these files etc/skel , /etc/login.defs  , /etc/default/useradd
``` bash
useradd -D  
```

>[!tip] see info about users
>/etc/passwd ,  /etc/shadow ,  /etc/group

