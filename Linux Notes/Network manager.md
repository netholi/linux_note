---
category: Networking
---

>[!note] 
>Most common on **Ubuntu, Fedora, GNOME, KDE, etc.**
>**nmcli** - command-line tool for controlling Network Manager

#### Cheat sheet
$curl cheat.sh/nmcli

``` bash
$ nmcli connection show
$ nmcli --help
$ nmcli d wifi show-password

```

##### Connect to Wi-Fi
- Turn on Wi-Fi:  
    `nmcli radio wifi on`

- Scan for available networks:  
    `nmcli device wifi rescan`

- List available networks and find your target SSID:  
    `nmcli device wifi list`

- Connect to the Wi-Fi network (replace with your exact network details):  
    `nmcli device wifi connect "YOUR_SSID" password "YOUR_PASSWORD"`

---


-  Example: `nmcli --help` or `nmcli general --help`   
  
- **View Connections:** List all connections (active and passive).
    - Example: `nmcli connection` (or `nmcli c`) 
      
- **Filter Active Connections:** Shows only currently active network connections.
    - Example: `nmcli connection show --active` 
      
- **List Wi-Fi Networks:** Scans for available Wi-Fi networks in your area.
    - Example: `nmcli device wifi list` 
      
- **Connect to Wi-Fi:** Connects to a specific network by SSID.
    - Example: `nmcli device wifi connect SSID_NAME password PASSWORD` 
      
- **Show Wi-Fi QR/Password:** Prints a QR code and passphrase to the terminal for easy mobile connection.
    - Example: `nmcli device wifi show-password`
      
- **Device Status:** Checks the status of networking devices.
    - Example: `nmcli device status` 
      
- **Bring Connection Down:** Disconnects from a specific network using its UUID.
    - Example: `nmcli connection down UUID` 
      
- **Bring Connection Up:** Connects to a specific network using its UUID.
    - Example: `nmcli connection up UUID` 