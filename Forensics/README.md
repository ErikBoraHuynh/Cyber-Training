## Intro to Digital Forensics Completion
<img width="1920" height="400" alt="Forensics" src="https://github.com/user-attachments/assets/9e83bbb9-a114-443e-9dbc-a805c23ebe03" />

## PicoCTF Completion

### Hidden in plainsight:

1. Downloaded the file using **wget https://challenge-files.picoctf.net/c_amiable_citadel/58f49cf585a3e6073ccd6a3ae03903dfd71567a2db9101645b428ac6820fb3cf/img.jpg**
   
2. Verified that the file is downloaded using **ls**
   
3. Read the file's metadata using **exiftool img.jpg**
   
4. Noticed that the comment c3RlZ2hpZGU6Y0VGNmVuZHZjbVE9 in the file's metadata is a Base64 string. Decoded it using **echo "c3RlZ2hpZGU6Y0VGNmVuZHZjbVE9" | base64 -d** to get the output **steghide:cEF6endvcmQ=**
   
5. Noticed that the output cEF6endvcmQ= is also a Base64 string. Decoded it using **echo "cEF6endvcmQ=" | base64 -d** to get the output **pAzzword**
   
6. Noticed that this makes "steghide:cEF6endvcmQ=" also mean "steghide:pAzzword". Knowing steghide is a steganography tool, I used **steghide extract -sf img.jpg -p pAzzword** to get the output "flag.txt"

7. Verified that flag.txt is downloaded using **ls**

8. Displayed the contents of flag.txt using **cat flag.txt** to get the CTF flag

<img width="599" height="806" alt="PicoCTF Forensics 1" src="https://github.com/user-attachments/assets/59afffcd-b559-4740-8a5b-98c497f471e6" />

***

image
test
***

image
test
***

image
test
***

image
test
***

image
test
