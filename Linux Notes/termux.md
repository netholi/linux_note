To access your Android device's shared internal storage using Termux, you must run the termux-setup-storage command. This command requests system-level file access permissions and automatically creates a directory layout mapping to your local folders

Open Termux on your Android device.Run the setup utility by typing the following command and pressing Enter:
``` shell
termux-setup-storage
```

*Allow access when the Android system pop-up asks you to grant storage permissions to Termux.* 

Navigating Your Folders. Once permission is granted, a new folder named storage will be created in your Termux home directory (~/storage). You can type cd ~/storage and run ls to view symlinks directly routing to your local files:

>[!note] Common Troubleshooting
	Fix "Permission Denied" ErrorsIf you run ls ~/storage/shared and encounter a "Permission Denied" error (common on newer versions like Android 14), follow this simple reset trick:
	
- Minimize Termux and open your system Android Settings.
- Go to Apps > Termux > Permissions.
- Turn Storage permission Off (Revoke).
- Turn Storage permission back On (Grant).


>[!note] Server Configuration inside Termux

Update local package repositories and existing packages
``` shell
pkg update && pkg upgrade
```

Install the OpenSSH suite
``` shell
pkg install openssh
```

Set a secure login password for your Termux user account
``` shell
passwd
```

Retrieve your system-assigned unique user identifier
``` shell
whoami
```


*Note down the value returned by `whoami` (it typically looks like `u0_a123` or similar). You will need it to authenticate the remote session.*

>[!note] Managing the Server State

Control the operational status of your background daemon using the following system binaries:

- **Start Server:** Type `sshd` and hit enter. The process runs detached in the background silently.

- **Prevent Sleep:** Run `termux-wake-lock` to acquire an execution lock. This stops the Android OS from sleeping the background process when the screen turns off.

- **Stop Server:** Kill active service processes safely by executing `pkill sshd`. 


>[!note] Establishing a Remote Client Connection

``` shell
ssh <username>@<ip_address> -p 8022
```

>[!note] Opening App on phone
Using the Android Activity Manager

The general command structure is: 
am start -n [package.name]/[activity.name]

start google
``` shell
am start -n com.android.chrome/com.google.android.apps.chrome.Main
```

youtube

``` shell
am start -n 
com.google.android.youtube/com.google.android.apps.youtube.app.watchwhile.WatchWhileActivity
```
_Note: You can find specific application package names and exact internal activity paths by using third-party APK inspecting apps from repositories like [F-Droid](https://f-droid.org/packages/com.termux/)._ [[1](https://www.reddit.com/r/termux/comments/1gcjcxk/opening_apps_in_termux/), [2](https://f-droid.org/packages/com.termux/)]



>[!note] Method 2: Using the Termux-Open Utility
If you want to trigger an app implicitly by opening a file or web link, use the `termux-open` command. This prompts Android to launch the default application mapped to that specific item or file type

``` shell
termux-open https://www.google.com
termux-open /sdcard/Download/photo.jpg
```

>[note] Take photo

###### install termux api from fdroid

``` shell
pm list packages | grep termux.api
```

 - c1 front camera c 0 back camera
``` shell
termux-camera-photo -c 1 my_photo2.jpg
```

move photo to picture folder
``` shell
mv my_photo.jpg ~/storage/pictures/
```



Create a file named `snap.sh`:
bash

```
#!/bin/bash
# Generate a filename using the current date and time
FILENAME="photo_$(date +%Y%m%d_%H%M%S).jpg"

# Take the photo using the rear camera (0)
termux-camera-photo -c 0 "$FILENAME"

echo "Photo saved as $FILENAME"
```

Run it by typing: `chmod +x snap.sh && ./snap.sh`


``` shell
termux-camera-info
termux-toast "Hello"
```

###### Clear Stuck Background Tasks

Sometimes the background bridge gets stuck in a loop. Kill the active session by running:

```
pkill -f com.termux.api
```
