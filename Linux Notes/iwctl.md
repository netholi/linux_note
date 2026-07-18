---
title: iwctl
created: 2026-07-18
---
#### 🔸 **iwd**  * (iNet wireless daemon)*
>[!note] Note
> A modern replacement for `wpa_supplicant` developed by Intel.
>  Fast, clean, and integrates well with `systemd-networkd`.

``` shell
$iwctl
[iwd]# device list`
```
`Devices` 

| Name | Address | Powered | Adapter | Mode |
|-------|:------:|:-------:|----------|-------|
|wlan0 | 34:68:95:3f:af:1d | on | phy0 | station|

```bash
[iwd]# station wlan0 scan
[iwd]# station  wlan0 get-networks
```


 `Available networks`

| Network name           | Security           | Signal  |
| ---------------------- |:----------------:  | ------  |
|  KCV_DataOnline        |     psk            |    **** |
|  KCV_DataOnline_5G     |     psk            |    **** |
| AndroidAP6569          |     psk            |    **** |

``` bash
[iwd]# station wlan0 connect AndroidAP6569
[iwd]# station wlan0 show`
[iwd]# quit
```