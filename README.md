# Install Ubuntu-18.04-LST on Zynq-7000

## Environment

 Virtual Machine: VMware-Workstation-16-Pro

 Operating System: Ubuntu-16.04-LST

 Development Board: Zynq-AC7021B

## How to use this project
### **If your development board is Zynq-7000** 

You can probably just copy my uploaded files (BOOT.bin, image.ub, rootfs) to the SD card of your board to install the Ubuntu-18.04.5 on it:

1. Partition the SD card to FAT (the first volume) and EXT4 (the second volume);

2. Use `sudo cat xaa xab xac > ubuntu-rootfs.tar.gz` to obtain the `ubuntu-rootfs.tar.gz`;

3. Use `sudo tar -zxvf ubuntu-rootfs.tar.gz -C ./` to gain the rootfs;

4. Copy the BOOT.bin and image.ub to the FAT volume, and the rootfs to the EXT4 volume;

5. Get a Ubuntu-18.04 without GUI on your board, you can use serial connection to control your SoC directly. 

The password of root, user's name and user's password are all `zynq`.

### **If your development board is not Zynq-7000** 

You may need to build your own BOOT.bin and image.ub based on your SoC architecture since the generated `.hdf/.xsa` file could be different with mine.

You could take my Guide (upload later sometime) as a reference to your installation process. 

## Unsolved warning messages (not hinder the usage, may fix later)

### 1. Failed to start Create Volatile Files and Directories

This may be caused by the access permission of some system directories. This seems impact nothing.

### 2. Failed to start Network Name Resolution
This may be caused beacuse `systemd-resolved.service` was not running. You can avoid this by mounting the SD card to your Ubuntu in virtual machine to install the package you need.

### 3. sudo: unable to stat /etc/sudoers
This could happen when use `sudo` commands, may be caused be the user's permission. You can avoid this situation by use `su` to convert to `root` to run the wanted commands with root permission.

