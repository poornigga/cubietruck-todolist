# Cubiereuck Bus System

## Download
download the [cubietruck lubuntu](http://dl.cubieboard.org/software/a20-cubietruck/lubuntu/ct-lubuntu-nand-v2.0/server/ct-lubuntu-server-nand-v2.0.img.gz) distribution.

## Initialization
1. decompress the image and burn it to the board by LiveSuit/PhonixSuit.
2. boot the system, and login, username `linaro`, password `linaro`
3. the root's password is empty, so set one, `sudo password root`
4. update your repo, `sudo apt-get update`

## Wifi AP Config
1. get `hostapd`, `sudo apt-get install -y hostapd`
2. edit config file `/etc/hostapd/hostapd.conf`
