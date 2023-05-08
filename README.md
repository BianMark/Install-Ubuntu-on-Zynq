# Install Ubuntu-18.04-LST on Zynq-7000

## Environment
Virtual Machine: Ubuntu-16.04-LST on VMware-Workstation-16-Pro

Board Version: Zynq-AC7021B

## How to use this project
**If your development board is Zynq-7000** 

You can probably just copy my uploaded files (BOOT.bin, image.ub, rootfs) to the SD card of your board to install the Ubuntu-18.04.5 on it:

1. Partition the SD card to FAT (the first volume) and EXT4 (the second volume);

2. Use `sudo cat xaa xab xac > ubuntu-rootfs.tar.gz` to obtain the `ubuntu-rootfs.tar.gz`;

3. Use `sudo tar -zxvf ubuntu-rootfs.tar.gz -C ./` to gain the rootfs;

4. Copy the BOOT.bin and image.ub to the FAT volume, and the rootfs to the EXT4 volume;

5. Get a Ubuntu18.04 without GUI on your board, you can use serial connection to control your SoC directly.

**If your development board is not Zynq-7000** 

You may need to build your own BOOT.bin and image.ub based on your SoC architecture since the generated `.hdf/.xsa` file could be different with mine.

You could take my Guide (upload later sometime) as a reference to your installation process. 
