# Install Ubuntu-18.04-LST on Zynq-7000

## Environment
Ubuntu-16.04-LST on VMware-Workstation-16-Pro

Zynq AC7021B

## How to use this project
### If your SoC board is Zynq-7000, you can probably just copy my uploaded files (BOOT.bin, image.ub, rootfs) to the SD card of your board to install the Ubuntu-18.04.5 on it. 

The SD card need to be partitioned to FAT(the first volume) and EXT4(the second volume), then copy the BOOT.bin and image.ub to the FAT volume, and the rootfs(obtained by `tar` the ubuntu-rootfs.tar.gz), and you can get a Ubuntu18.04 without GUI.

### If your development board is not Zynq-7000, you can look the Guide(upload later sometime) as a reference to your installation process.
