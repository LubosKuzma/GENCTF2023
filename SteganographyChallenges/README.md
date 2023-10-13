# Steganography Challenges List
****

## Challenge 1 (Different)
  - **Category**: Steganography
  - **Description**: Brute force the passphrase to access the hidden text file within the image, where the flag is concealed in the file.
  - **Flag**: GENCTF{OBFU5CAT3D_FLAG}
  - **Quick Guide**: First use a steganography tool like stegcracker which allows bruteforce of passpharase on the image to find the zip file hidden in the image find the compression method (.gz) and decompress it to find the text file, then either creaet a python script or suitable method to filter flag out of the obfuscated data in the text file (removing all the lowercase letters or filter only uppercase letter,digits and special character from text file which is the flag).
  - **Hint** - Within the ordinary, seek the extraordinary. Look for the elements that defies the pattern.

## Challenge 2 (Lion Rock)
  - **Category**: Steganography/Osint
  - **Description**: Participants are given a image with a zip and text file hidden in it using steganography which can extracted by entering a passpharase which will be hidden in the metadata of the image. The zip file is password protected which the particiant need will crack to get the flag (the password for zip file will not be simple rockyou list but the player have to apply specail rules to crack the password hashes) and the text file with zip file will have a hint regarding the possible password for zip file.
  - **Flag**: GENCTF{Pl@y1ng_W!th_Rul35}
  - **Quick Guide**: First use tools like exiftool to search the image metadata for password (P4ssword123456) which can be used to extract file hidden in the image. Once the text file and password protected zip file are extracted, read the text file which contains a hint for the password used for the zip file. Reverse search the image provided as the cover image or the original file which will shows the results **Sigiriya** and use the hints in the text file (which mentions to use rules to change i -> 1 and a ->4) and use the password (S1g1r1y4) to extract flag from the zip flag.
    
## Challenge 3 
  - **Category**: Steganography
  - **Description**: In this challenge, participants are tasked with uncovering a secret message hidden within an image. The flag is concealed in the Least Significant Byte (LSB) of the image's pixel data.
  - **Flag**: GENCTF{S3cr3t_Fl@g_2023}
  - **Quick Guide**: To solve the challenge either use a online available tool or create a python script which can extract data hidden in Least signficant byte of the image and the message extracted is the flag.

## Challenge 4
  - **Category**: Steganography
  - **Description**: In this steganography challenge, participants are presented with an image that conceals a hidden text file. To extract the text file from the image, you must uncover the passphrase, which is ingeniously hidden within the image itself in base64 encoded format. The extracted text file contains base64-encoded data, which, when decoded, transforms into an image. This image is a QR code that, when scanned, reveals the coveted flag.
  - **Flag**: GENCTF{B@se64_T0_Im@g3}
  - **Quick Guide**: First find the base64 encoded password (S3cureP455w0rd) hidden in the image file using tools like binwalk, base64 deocde the passpharse and use it to extract the text file from the image. The text file will have base64 data which can be converted to image using online base64 to image converter tools. The image from this conversion is a qr code, which can read using qr code reader and this contains the flag.
  - **Hint**: Base64 can be deocded into more than just text.

## Challenge 5
  - **Category**: Steganography
  - **Description**: This steganography challenge, participants will be given a audio file which has a message hidden inside the file without any passphrase used. The message hidden is encoded with Caesar cipher, which the player have to solve to get the flag.
  - **Flag**:GENCTF{Aud10_St3g@n0gr@phy}
  - **Quick Guide**: Use tools like steghide to extract the message hidden in the audio file (since no passphrase is used the message can extracted while leaving the passphrase empty). Once the hidden message is extracted which is encrypted using Ceasr Cipher, use a online tools to brute force the encrypted text to get the flag.

## Challenge 6
  - **Category**: Steganography
  - **Description**: 
  - **Flag**: 
  - **Quick Guide**: 

