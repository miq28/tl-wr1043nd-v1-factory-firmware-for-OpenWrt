This firmware shall be used to restore OpenWrt back to Tp-Link factory OS.
The boot code has been stripped using the following command: 

$ dd if=wr1043nv1_en_3_13_13_up_boot\(130428\).bin of=wr1043nd_v1_correct.bin skip=257 bs=512

Firmware update
Copy this file to router /tmp folder. The easiest way is logging-in to your router via ssh using WinScp.

Write the firmware to flash
Use this command:
root@OpenWrt:~# mtd -r write /tmp/wr1043nv1_en_3_13_15_up_boot(140319)_corrected.bin firmware

Wait until “Rebooting …” appears

Go to http://192.168.1.1 in your browser after finishing the flashing process.

Default factory credential is:

user:	admin
password:	admin
