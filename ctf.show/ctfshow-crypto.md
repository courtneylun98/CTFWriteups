# CTF.Show - Crypto (CTF秀 - 解密)

**This page will be in a mixutre of Chinese and English just becasue the platform is in Simplifed Chinese but I'm yet to be comfortable writing writeups in Chinese.**

Platform: [CTF.Show](https://ctf.show/)

## 密码学签到

### Question:
}wohs.ftc{galf

### Steps:
Just flip the order. Since it is so short, it is unneccessary to write a script for it.

### Flag:
> flag{ctf.show}


## crypto2

### Question:
A txt file.

### Steps:
Seeing that the ciphertext only contains ()[]!+ , we can safely assume that it was encoded with JSFuck. Using a decoder, we were able to obtain the flag.

### Flag:
> flag{3e858ccd79287cfe8509f15a71b4c45d}


## crypto3

### Question:
txt file.

### Steps:
From a string cute japanese emojis as ciphertext, we can tell that the it has used aaencode for encryption. Run the string through a decoder and we will get the flag.

### Flag:
> flag{js_da_fa_hao}


## crypto4

### Question:
p=447685307 q=2037 e=17

提交flag{d}即可

### Steps:
p, q, d and e hints us towards RSA encryption. The forumula for d is:
> d == e modInverse (p-1)(q-1)

Passing this into a calculator and we will get the answer for the flag.


### Flag:
> flag{53616899001}


## crypto0

### Question:
gmbh{ifmmp_dug}

### Steps:
Run it through a ceaser cipher to bruteforce for every possiblity due to the fact that the ciphertext still contains the structure and the amount of characters in front (flag) has not change.

### Flag:
> flag{hello_ctf}
