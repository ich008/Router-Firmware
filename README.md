# Router-Firmware
Custom OpenWrt Builds &amp; Recovery &amp; dumps

USAGE ON YOUR OWN RISK!

D7 flashing 
 1. Press any key to stop autobooting and obtain U-Boot CLI access.
 2. Setup ip addresses for U-Boot and your tftp server.
 3. Issue below commands:
    tftp 0x81000000 [name of your firmware file].bin
    erase 0x9f020000 +f80000
    cp.b 0x81000000 0x9f020000 $filesize
    reset
    
D7 run from RAM:
 1. Press any key to stop autobooting and obtain U-Boot CLI access.
 2. Setup ip addresses for U-Boot and your tftp server.
 3. Issue below commands:
	tftpboot 0x81000000 initramfs-kernel.bin
	bootm 0x81000000
  
