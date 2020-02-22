# CTF.Show WriteUp

#### This page will be a mixutre of Chinese and English just becasue the platform is in Chinese but I'm not sure on the terminologies in Chinese.

Platform: [CTF.Show](https://ctf.show/)


## 萌新认证

This flag is for accessing the questions for newbies, it can only be aquired by heading to the QQ group chat and asking the group owner.


## 萌新_密码1

###Question:
密文： 53316C6B5A6A42684D3256695A44566A4E47526A4D5459774C5556375A6D49324D32566C4D4449354F4749345A6A526B4F48303D

提交格式：KEY{XXXXXXXXXXXXXX}

### Steps:
As the encoded string does not contain a character larger than F, we can assume that it is Hex. 
From that we got a Base64 string, decode that and we get a string that seems like a simple rail fence cipher.
Run it through a rail fence cipher decoder and you will get the flag.

### Flag:
> KEY{dffb06a33eeeb0d259c84bd8cf146d08-}



## 萌新_密码2

### Question:
出题人已累，随便敲了几下键盘。。。 rdcvbg 2qase3 6tghu7

flag格式KEY{XXXXXX}

### Steps:
Looking at the hints provided in the text, it tells you that the person is tired and pressed on the keyboard randomly. Taking that as a hint and looking at the keyboard, we can see that each set of characters creates a circle around a letter. With the three letters combined, we have our flag.

### Flag:
> KEY{f w y}



## 萌新 密码3

### Question: 

题目名称：我想吃培根 题目描述： -- --- .-. ... . ..--.- .. ... ..--.- -.-. --- --- .-.. ..--.- -... ..- - ..--.- -... .- -.-. --- -. ..--.- .. ... ..--.- -.-. --- --- .-.. . .-. ..--.- -- -- -.. -.. -- -.. -- -.. -- -- -- -.. -.. -.. /-- -.. -- -.. -.. --/ -- -- -- -- -- /-- -.. -.. -- -.. -- /-- -.. -.. -- 

格式：flag{***********}

### Steps:
It's quite obivious that this is morse code so run it through a morse code decoder. 

From that we get the output:

> MORSE_IS_COOL_BUT_BACON_IS_COOLER_MMDDMDMDMMMDDD MDMDDM MMMMM MDDMDM MDDM

From the title of the question (I want to eat bacon) and the output we got, we can safely assume that it is referring to the Bacon Cipher.

Replacing the Ms with A and Ds with B and running it through a decoder, we get the output:

> GUOWANG

This will be the text within the flag.

### Flag:

> flag{GUOWANG}


## 萌新 密码#4

### Question:
QW8obWdIWF5FKUFSQW5URihKXWZAJmx0OzYiLg==

### Steps:
Decoding the string we get the following string:

> Ao(mgHX^E)ARAnTF(J]f@&lt;6".

Running this through a Base85 decoder and we will get the flag.

### Flag:
> flag{base_base_base}


## 萌新 隐写3

### Question:
![Rookie Stego](image/rookie/rookie_stego3.jpg)

### Steps:
The flag is on the image.

### Flag:
> flag{xinti_gkd}
