# BUUCTF - Crypto

**This page will be in a mixutre of Chinese and English just becasue the platform is in Simplifed Chinese but I'm yet to be comfortable writing writeups in Chinese.**

Platform: [BUUCTF](https://buuoj.cn/)

## MD5

### Question:
zip with ciphertext: e00cf25ad42683b3df678c61f42c6bda

### Steps:
Taking the hint in the title, use a MD5 hash cracker to get the answer for the flag.

### Flag:
> flag{admin1}


## 看我回旋踢

### Question:
zip with ciphertext: synt{5pq1004q-86n5-46q8-o720-oro5on0417r1}

### Steps:
Taking the hint in the title (mentions of a spin kick), the cipher used probably has to do with Rot. Run it through a rot decoder and bruteforce for all possiblity to obtain flag.

### Flag:
> flag{5cd1004d-86a5-46d8-b720-beb5ba0417e1}


## Url编码

### Question:
zip with ciphertext: %66%6c%61%67%7b%61%6e%64%20%31%3d%31%7d

### Steps:
Taking the hint in the title, run it through a url encoding decoder for flag.

### Flag:
> flag{and 1=1}


## 一眼就解密

### Question:
下面的字符串解密后便能获得flag：ZmxhZ3tUSEVfRkxBR19PRl9USElTX1NUUklOR30=  
注意：得到的 flag 请包上 flag{} 提交

### Steps:
From looking at the string, an obvious base64. Run it through a decoder for flag.

### Flag:
> flag{THE_FLAG_OF_THIS_STRING}


## 摩丝

### Question:
zip with ciphertext: .. .-.. --- ...- . -.-- --- ..-

### Steps:
Obvious morse, run it through decoder for flag.

### Flag:
> flag{ILOVEYOU}


## Quoted-printable

### Question:
zip with ciphertext: =E9=82=A3=E4=BD=A0=E4=B9=9F=E5=BE=88=E6=A3=92=E5=93=A6

### Steps:
Obvious hex, run it through decoder for flag.

### Flag:
> flag{那你也很棒哦}

