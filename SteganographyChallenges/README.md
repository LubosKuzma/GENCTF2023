# Steganography Challenges List
****

## Challenge 1 
  - **Category**: Steganography
  - **Description**: Participants need to find the hidden text file containing the flag (flag which contains either Uppercase letter and special characters will be obfuscated in a large number of lowercase letter) within an image using steganography techniques. The text file is extractable using a passphrase, which they must brute force.
  - **Flag**: CTF{0BFU5C@t3D_FL4G}
  - **Quick Guide**: First use a steganography tool like stegcracker which allows bruteforce of passpharase on the image to find the text file hidden in the image, then either creaet a python script or suitable method to filter flag out of the obfuscated data in the text file (removing all the lowercase letters or filter only uppercase letter and special character from text file which is the flag).
  - **Hint** - Within the ordinary, seek the extraordinary. Look for the one element that defies the pattern.

## Challenge 2
  - **Category**: Steganography
  - **Description**: Participants are given a image with a zip and text file hidden in it using steganography which can extracted by entering a passpharase which will be hidden in the metadata of the image. The zip file is password protected which the particiant need will crack to get the flag (the password for zip file will not be simple rockyou list but the player have to apply specail rules to crack the password hashes) and the text file with zip file will have a hint regarding the possible password for zip file.
  - **Flag**: CTF{Pl@y1ng_W!th_Rul35}
  - **Quick Guide**: First use tools like exiftool to search the image metadata for passpharse which can be used to extract file hidden in the image. Once the text and password protected zip files are extracted, read the text file which contains a hint for the password used for the zip file. Then use tools like john the ripper to create hashes of the zip file and define a rule in JTR which changes all letter a/A to 4, now use rockyou.txt list to brute force the hashes for the zip file.

## Challenge 3 
  - **Category**: Steganography
  - **Description**: In this challenge, participants are tasked with uncovering a secret message hidden within an image. The flag is concealed in the Least Significant Byte (LSB) of the image's pixel data. Your mission is to extract the hidden message.
  - **Flag**: CTF{S3cr3t_Fl@g_2023}
  - **Quick Guide**: To solve the challenge either use a online available tool or create a python script which can extract data hidden in Least signficant byte of the image and the message extracted is the flag.

## Challenge 4
  - **Category**: Steganography
  - **Description**: 
  - **Flag**: 
  - **Quick Guide**: 

## Challenge 5
  - **Category**: Steganography
  - **Description**: 
  - **Flag**: 
  - **Quick Guide**:

## Challenge 6
  - **Category**: Steganography
  - **Description**: 
  - **Flag**: 
  - **Quick Guide**: 

