# How to mount an external drive
## Mount drive
### Find the drive
In a first step, you have to find the drive to be mounted in the system. Usually, the drive has the name sd_[number] (e.g. sdb1). 

`lsblk`

### If not existing, create new directory
The new drive should be mounted to a directory under /media/. If no directory exists there or no directory is free, create a new one

`sudo mkdir /media/new_directory`

### Mount the drive
In the last step, mount the drive to the chosen directory

`sudo mount /dev/sd_[number] /media/new_directory`
e.g. `sudo mount /dev/sdb1 /media/new_directory`

## Unmount drive
### Unmount drive
Unmount the drive using the appropriate command

`sudo umount /media/new_directory`

### Check whether drive is unmounted
If the drive is unmounted, the command lsblk doesn't list any mount point for the drive

`lsblk`
