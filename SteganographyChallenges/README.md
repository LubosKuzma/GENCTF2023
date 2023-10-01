# Steganography Challenges List
****

## Challenge 1 
  - **Category**: Steganography
  - **Description**: Participants need to find the hidden text file containing the flag (flag which contains either Uppercase letter and special characters will be obfuscated in a large number of lowercase letter) within an image using steganography techniques. The text file is extractable using a passphrase, which they must brute force.
  - **Flag**: CTF{0BFU5C@t3D_FL4G}
  - **Quick Guide**: First use a steganography tool like stegcracker which allows bruteforce of passpharase on the image to find the text file hidden in the image, then either creaet a python script or suitable method to filter flag out of the obfuscated data in the text file (removing all the lowercase letters or filter only uppercase letter and special character from text file which is the flag).
  - **Hint** - Within the ordinary, seek the extraordinary. Look for the elements that defies the pattern.

## Challenge 2
  - **Category**: Steganography
  - **Description**: Participants are given a image with a zip and text file hidden in it using steganography which can extracted by entering a passpharase which will be hidden in the metadata of the image. The zip file is password protected which the particiant need will crack to get the flag (the password for zip file will not be simple rockyou list but the player have to apply specail rules to crack the password hashes) and the text file with zip file will have a hint regarding the possible password for zip file.
  - **Flag**: CTF{Pl@y1ng_W!th_Rul35}
  - **Quick Guide**: First use tools like exiftool to search the image metadata for passpharse which can be used to extract file hidden in the image. Once the text and password protected zip files are extracted, read the text file which contains a hint for the password used for the zip file. Then use tools like john the ripper to create hashes of the zip file and define a rule in JTR which changes all letter a/A to 4, now use rockyou.txt list to brute force the hashes for the zip file.

## Challenge 3 
  - **Category**: Steganography
  - **Description**: In this challenge, participants are tasked with uncovering a secret message hidden within an image. The flag is concealed in the Least Significant Byte (LSB) of the image's pixel data.
  - **Flag**: CTF{S3cr3t_Fl@g_2023}
  - **Quick Guide**: To solve the challenge either use a online available tool or create a python script which can extract data hidden in Least signficant byte of the image and the message extracted is the flag.

## Challenge 4
  - **Category**: Steganography
  - **Description**: In this steganography challenge, participants are presented with an image that conceals a hidden text file. To extract the text file from the image, you must uncover the passphrase, which is ingeniously hidden within the image itself in base64 encoded format. The extracted text file contains base64-encoded data, which, when decoded, transforms into an image. This image is a QR code that, when scanned, reveals the coveted flag.
  - **Flag**: CTF{B@se64_T0_Im@g3}
  - **Quick Guide**: First find the base64 encoded passpharse hidden in the image file using tools like binwalk, base64 deocde the passpharse and use it to extract the text file from the image. The text file will have base64 data which can be converted to image using online base64 to image converter tools. The image from this conversion is a qr code, which can read using qr code reader and this contains the flag.
  - **Hint**: Think about how you can convert this data into something visual, something that might hide another secret.

## Challenge 5
  - **Category**: Steganography
  - **Description**: This steganography challenge, participants will be given a audio file which has a message hidden inside the file without any passphrase used. The message hidden is encoded with Caesar cipher, which the player have to solve to get the flag.
  - **Flag**: CTF{Aud10_St3g@n0gr@phy}
  - **Quick Guide**: Use tools like steghide to extract the message hidden in the audio file (since no passphrase is used the message can extracted while leaving the passphrase empty). Once the hidden message is extracted which is encrypted using Ceasr Cipher, use a online tools to brute force the encrypted text to get the flag.

## Challenge 6
  - **Category**: Steganography
  - **Description**: 
  - **Flag**: 
  - **Quick Guide**: 

