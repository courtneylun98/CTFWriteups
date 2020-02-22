# CTF.Show WriteUp

#### This page will be a mixutre of Chinese and English just becasue the platform is in Chinese but I'm not sure on the terminologies in Chinese.

Platform: [CTF.Show](https://ctf.show/)

***

### 萌新认证

This flag is for accessing the questions for newbies, it can only be aquired by heading to the QQ group chat and asking the group owner.

***

### 萌新_密码1

####Question:
密文： 53316C6B5A6A42684D3256695A44566A4E47526A4D5459774C5556375A6D49324D32566C4D4449354F4749345A6A526B4F48303D

提交格式：KEY{XXXXXXXXXXXXXX}

#### Steps:
As the encoded string does not contain a character larger than F, we can assume that it is Hex. 
From that we got a Base64 string, decode that and we get a string that seems like a simple rail fence cipher.
Run it through a rail fence cipher decoder and you will get the flag.

#### Flag:
> KEY{dffb06a33eeeb0d259c84bd8cf146d08-}

***

### 萌新_密码2

#### Question:
出题人已累，随便敲了几下键盘。。。 rdcvbg 2qase3 6tghu7

flag格式KEY{XXXXXX}

##### Steps:
Looking at the hints provided in the text, it tells you that the person is tired and pressed on the keyboard randomly. Taking that as a hint and looking at the keyboard, we can see that each set of characters creates a circle around a letter. With the three letters combined, we have our flag.

#### Flag:
> KEY{f w y}

***
