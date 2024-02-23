# CSI

Cyber Security
Task 1: Wireshark capture
I downloaded the file and opened it in wireshark and noticed that someone with an IP of 192.168.49.134 is sending its username and password in an un-encrypted manner.
84 Request: USER 0ffs3cUs3r3
99 Response: 331 Username ok, send password.
93 Request: PASS very_secret_password
89 Response: 230 Login successful.

![image](https://github.com/HAC20KER22/CSI/assets/114013658/3b423a91-df1c-46a6-a1ea-c29d1647c80f)

Task 2: Sound.wav File
I started with metadata and got to know that its a RIFF file, but that didn't lead me anywhere. SO I started searching for another type of analysis on a .wav file and found spectral analysis. 
I found "flag: e5353bb7b57578bd4da1c898a8e2d767" through spectral analysis. 

Task 3: Encrypted.txt
I started with metadata in the file and got a pattern of 09 and 20 I checked and found that they are codes for spaces in hex, so first I checked by replacing 09 with 0 and 20 with 1 , but only with the headers and got something rubbish. Then I checked replaced 09 with 1 and 20 with 0 and with the whole file by converting the blanck spaces into hex and then replacing those in binary. Then making sets of 8, I got the flag I needed.
The binary code for flag:
01100011 01110011 01101001 01111011 01101110 01101111 01110100 01011111 01100001 01101100 01101100 01011111 01110011 01110000 01100001 01100011 01100101 01110011 01011111 01100001 01110010 01100101 01011111 01100010 01101111 01110010 01101110 01011111 01110100 01101000 01100101 01011111 01110011 01100001 01101101 01100101 01111101

Flag: "csi{not_all_spaces_are_born_the_same}"
