# CTF.Show - Misc (CTF秀 - 雜項)

**This page will be in a mixutre of Chinese and English just becasue the platform is in Simplifed Chinese but I'm yet to be comfortable writing writeups in Chinese.**

Platform: [CTF.Show](https://ctf.show/)

## 杂项签到

### Question:
Zip file

### Steps:
(According to hex, I believe this show be a false encryption but MacOS is able to disregard it and unzip it without fault.)
Changing the 09 00 after 50 4B 01 02 1F 00 14 00 should resolve the false encryption. flag.txt within the folder contains the flag.


### Flag:
> flag{79ddfa61bda03defa7bfd8d702a656e4}


## misc2

### Question:
偶然发现我竟然还有个软盘，勾起了我的回忆。
	- A zip file

### Steps:
Unzipping the file, we get a FAT12 image. Create a new VM on VirtualBox/VMWare and load the floppy in as storage. Upon booting, the flag is displayed on screen.


### Flag:
> flag{ctfshow}

## misc3

### Question:
密文：zse4rfvsdf 6yjmko0

提示1：解密后两个字符,小写 提示2：看看自己下面

提交flag{明文}

### Steps:
Looking at the keyboard and trace the path of the characters mentioned accordingly. The two strings writes out as A and V on the keyboard.


### Flag:
> flag{AV}

