## Intro to Digital Forensics Completion
<img width="1920" height="400" alt="Forensics" src="https://github.com/user-attachments/assets/9e83bbb9-a114-443e-9dbc-a805c23ebe03" />

## PicoCTF Completion

### Hidden in plainsight:

1. Downloaded the file using **wget https://challenge-files.picoctf.net/c_amiable_citadel/58f49cf585a3e6073ccd6a3ae03903dfd71567a2db9101645b428ac6820fb3cf/img.jpg**
   
2. Verified that the file is downloaded using **ls**
   
3. Read the file's metadata using **exiftool img.jpg**
   
4. Noticed that the comment c3RlZ2hpZGU6Y0VGNmVuZHZjbVE9 in the file's metadata is a Base64 string. Decoded it using **echo "c3RlZ2hpZGU6Y0VGNmVuZHZjbVE9" | base64 -d** to get the output **steghide:cEF6endvcmQ=**
   
5. Noticed that the output cEF6endvcmQ= is also a Base64 string, especially hinted at with the = at the end. Decoded it using **echo "cEF6endvcmQ=" | base64 -d** to get the output **pAzzword**
   
6. Noticed that this makes "steghide:cEF6endvcmQ=" also mean "steghide:pAzzword". Knowing steghide is a steganography tool, I used **steghide extract -sf img.jpg -p pAzzword** to get the output "flag.txt"

7. Verified that flag.txt is downloaded using **ls**

8. Displayed the contents of flag.txt using **cat flag.txt** to get the PicoCTF flag

<img width="599" height="806" alt="PicoCTF Forensics 1" src="https://github.com/user-attachments/assets/59afffcd-b559-4740-8a5b-98c497f471e6" />

***

### Riddle Registry:

1. Downloaded the file using **wget https://challenge-files.picoctf.net/c_amiable_citadel/570d726d77600d7540c9a8fe7df9e37f4e8b05fafe16f2b316f4a0603dfa7d2f/confidential.pdf**

2. Verified that the file is downloaded using **ls**

3. Read the file's metadata using **exiftool confidential.pdf**

4. Noticed that the author cGljb0NURntwdXp6bDNkX20zdGFkYXRhX2YwdW5kIV9mOTQzMDBjNH0= in the file's metadata is a Base64 string, hinted at with the = at the end. Decoded it using **echo "cGljb0NURntwdXp6bDNkX20zdGFkYXRhX2YwdW5kIV9mOTQzMDBjNH0=" | base64 -d** to get the PicoCTF flag

<img width="1179" height="508" alt="PicoCTF Forensics 2" src="https://github.com/user-attachments/assets/1e9ae067-c30b-4a7c-84ce-c4aab7fc30aa" />

***

### Flag in Flame:

1. Downloaded the file directly in my Kali Linux VM

2. Verified that the file is downloaded using **cd Downloads** and then **ls**

3. After taking a look at the hint given in the challenge, which stated "Use base64 to decode the data and generate the image file.", I converted the logs.txt to an image using **cat logs.txt | base64 -d > logs_Decoded.jpg**

4. Noticed that the opened image contained the text that only has characters from 0-9 and A-F, indicating that it is written in hexadecimal

5. Decoded the hex text using **CyberChef** to get the PicoCTF flag

<img width="1609" height="939" alt="PicoCTF Forensics 3" src="https://github.com/user-attachments/assets/365f1712-c30a-451d-994d-d5a099847191" />
<img width="637" height="821" alt="PicoCTF Forensics 3 1" src="https://github.com/user-attachments/assets/62083d79-4049-4cd1-9d63-ade1e6b11fee" />
<img width="1530" height="886" alt="PicoCTF Forensics 3 2" src="https://github.com/user-attachments/assets/e0590549-aec0-4bfc-952d-c666c0b0d647" />

***

### DISKO 1:

1. Downloaded the file directly in my Kali Linux VM

2. Verified that the file is downloaded using **cd Downloads** and then **ls**

3. Noticed the file is compressed, hinted at with .gz at the end. Decompressed the file using **gzip -d disko-1.dd.gz**

4. After taking a look at the hint given in the challenge, which stated "Maybe Strings could help? If only there was a way to do that?", I displayed strings from the decompressed file using **strings disko-1.dd**

5. Decided to filter for the PicoCTF flag using **strings disko-1.dd | grep "flag"** but that did not work. Tried again with a different approach, using **strings disko-1.dd | grep "picoCTF"** to get the PicoCTF flag

<img width="950" height="925" alt="PicoCTF Forensics 4" src="https://github.com/user-attachments/assets/7b62140e-a3c5-4679-8d24-a5894dac3ef7" />
<img width="951" height="545" alt="PicoCTF Forensics 4 1" src="https://github.com/user-attachments/assets/9c28cd2c-82e6-4ce6-8bc2-c3e260b092f4" />
<img width="953" height="338" alt="PicoCTF Forensics 4 2" src="https://github.com/user-attachments/assets/1555f9dd-a284-4d38-b533-58fdf0e767ce" />

***

### Corrupted File:

1. Downloaded the file directly in my Kali Linux VM

2. Verified that the file is downloaded using **cd Downloads** and then **ls**

3. After taking a look at the hints 1, 2, and 3 given in the challenge, which stated "Try checking the file’s header.", "JPEG", and "Tools like xxd or hexdump can help you inspect and edit file bytes.", I analyzed the file's hexadecimal dump using **xxd file**

4. After research and considering hint 2, I learned that JPEG files start with "FF D8 FF E0" magic bytes. I noticed that the first four bytes of the file indicate that it is likely a JPEG file, but the first two bytes are corrupted. I create a new file with the corrected bytes by using **(printf '\xff\xd8' && tail -c +3 file) > file.jpg** to get the PicoCTF flag

<img width="954" height="602" alt="PicoCTF Forensics 5" src="https://github.com/user-attachments/assets/6012ec1d-d20f-407f-8fb3-ef6b9c9f2500" />
<img width="954" height="322" alt="PicoCTF Forensics 5 1" src="https://github.com/user-attachments/assets/4dcc6540-10aa-4239-8561-cb480282614b" />
<img width="798" height="493" alt="PicoCTF Forensics 5 2" src="https://github.com/user-attachments/assets/da21472c-13f7-461d-9765-3bda73a49e7e" />

***

### Secret of the Polyglot:

1. Downloaded the file directly in my Kali Linux VM

2. Verified that the file is downloaded using **cd Downloads** and then **ls**

3. After taking a look at the hint given in the challenge, which stated "This problem can be solved by just opening the file in different ways", I checked the file's hexadecimal dump using **xxd flag2of2-final.pdf**

4. Noticed that the first four bytes of the file are "89 50 4E 47", which indicates that it is a PNG file. I output a PNG version of the original PDF file by using **cat flag2of2-final.pdf > flag2of2-final.png**

5. Noticed that the text shown in the PDF file and the PNG file are in PicoCTF{flag} format. Combined the texts in both files to get the PicoCTF flag

<img width="954" height="348" alt="PicoCTF Forensics 6" src="https://github.com/user-attachments/assets/07b93eb0-9d4d-4f03-b525-0f335ca51d38" />
<img width="954" height="320" alt="PicoCTF Forensics 6 1" src="https://github.com/user-attachments/assets/14d7dd45-2ce5-4ac5-b458-517139399034" />
<img width="1150" height="629" alt="PicoCTF Forensics 6 2" src="https://github.com/user-attachments/assets/a5cb48a8-c70b-428d-9c4b-71cba97e7823" />
