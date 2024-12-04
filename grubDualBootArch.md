# Grub to detect windows install on arch

## TO check what Operating Systems are intalled on the device

    sudo efibootmgr -v 

## To make grup detect other Operating Systems that are installed

1. sudo -e /etc/default/grub 
2. add/uncomment `GRUB_DISABLE_OS_PROBER=false`
3. regenrate the grub config `sudo grub-mkconfig -o /boot/grub/grub.cfg`
