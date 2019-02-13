# Sticky-fingers-kali-pi 



## Download 
https://whitedome.com.au/re4son/sticky-fingers-kali-pi-pre-installed-image/

## Uncompress

xz -d StickyFingers-Kali-Pi-armhf-180923.img.xz

## Image your sd card

dd if=StickyFingers-Kali-Pi-armhf-180923.img of=/dev/mmcblk0 bs=512k


## Expanding partition to fill SDCard

https://whitedome.com.au/re4son/kali-pi/#fdisk


Reboot

resize2fs /dev/mmcblk0p2

## Install Virutal Keyboard

apt-get install florence


## Update Kernel

Stable repository

echo "deb http://http.re4son-kernel.com/re4son/ kali-pi main" > /etc/apt/sources.list.d/re4son.list
wget -O - https://re4son-kernel.com/keys/http/archive-key.asc | apt-key add -
apt update
apt install -y kalipi-kernel kalipi-bootloader kalipi-re4son-firmware kalipi-kernel-headers libraspberrypi0 libraspberrypi-dev libraspberrypi-doc libraspberrypi-bin
 

