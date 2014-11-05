# Cubiereuck Bus System

## Download
download the [cubietruck lubuntu](http://dl.cubieboard.org/software/a20-cubietruck/lubuntu/ct-lubuntu-nand-v2.0/server/ct-lubuntu-server-nand-v2.0.img.gz) distribution.

## Initialization
1. decompress the image and burn it to the board by LiveSuit/PhonixSuit.
2. boot the system, and login, username `linaro`, password `linaro`
3. the root's password is empty, so set one, `sudo password root`
4. update your repo, `sudo apt-get update`

## Wifi AP Config
+ get `hostapd`, `sudo apt-get install -y hostapd`
+ edit config file `/etc/hostapd/hostapd.conf`

like this

    interface=wlan0
    driver=nl80211
    ssid=cubietruck
    channel=11
    hw_mode=g
    macaddr_acl=0
    auth_algs=1
    ignore_broadcast_ssid=0

+ edit `/etc/modules`, change `bcmdhd` to `bcmdhd op_code=2`
+ reboot
+ startup hostapd, `sudo hostapd /etc/hostapd/hostapd.conf`

Now, you have a working AP!
