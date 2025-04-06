# Auto mounting a drive on linux

1. `mkdir` in /media/mountname
2. `sudo blkid` to get the UUID of the drive
3. `sudo -e /etc/fstab` add the UUID to fstab
4. `UUID=id *tab* /media/mountname *tab* ext4 *tab* defaults *tab* 0 *tab* 0`
5. `sudo mount -a`
