# BQS-5020
**Shift hex values ​​to make it work(for mkbootimg)! (0x80008000 >> 0x70008000)**

Need boot image information: 
* Boot magic: **ANDROID!**
* Kernel offset: **0x80008000**
* Ramdisk offset: **0x84000000**
* Second bootloader offset: **0x80f00000**
* Cmdline offset: **0x8e000000**
* Pagesize: **2048**
* Product name(board): **BQS-5020_6.0**

mkbootimg command: 
```
mkbootimg \
	--kernel KERNEL_PATH \
	--ramdisk RAMDISK_PATH \
	--kernel_offset 0x70008000 \
	--ramdisk_offset 0x74000000 \
	--second_offset 0x70f00000 \
	--tags_offset 0x7e000000 \
	--board BQS-5020_6.0 \
	--pagesize 2048 \
	-o boot.img
```
