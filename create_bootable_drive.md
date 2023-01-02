# How to create a bootable drive from a iso file
## Find the drive and unmount it
Find the drive with the command `lsblk`. Then unmount it with `sudo umount /dev/sd?`.

## Burn the image on the drive
This is a destructive command, hence be careful

`sudo dd bs=4M if=/path/to/input.iso of=/dev/sd? conv=fdatasync status=progress`
