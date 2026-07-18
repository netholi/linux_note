
Install flameshot (screen capture) and run in gui mode
``` bash
flameshot gui
```

>[!Warning] Error
flameshot: error: Screenshot portal timed out after 30 seconds flameshot: error: Unable to capture screen flameshot: info: Screenshot aborted.

>[!Info]- Try the following solutions to resolve the issue:
>Method 1: Enable the Legacy X11 Screenshot Method (Recommended)

>Users in the [Arch Linux Forums](https://bbs.archlinux.org/viewtopic.php?id=313917) suggest bypassing the portal if you are not using Wayland-native screen-grabbing backends. [(https://bbs.archlinux.org/viewtopic.php?id=313917)]

1. Open your terminal and open the Flameshot configuration file in a text editor (like nano):  
    ``` bash
    nano ~/.config/flameshot/flameshot.ini
    ```
    
2. Add the following line to the [General] section:  
    ```
    useX11LegacyScreenshot=true
    ```
    
3. Save the file and restart Flameshot. 
[(https://bbs.archlinux.org/viewtopic.php?id=313917), (https://forum.zorin.com/t/flameshot-does-not-work-anymore-after-some-time/31492)]


>[!Warning] Error

Flameshot gui Using deprecated legacy X11 screenshot method. Consider installing xdg-desktop-portal for your desktop. Future versions of Flameshot may remove the option to use the legacy method.

``` bash
sudo pacman -S xdg-desktop-portal xdg-desktop-portal-gtk
```

