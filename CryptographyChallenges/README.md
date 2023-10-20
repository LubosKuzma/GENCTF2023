# Cryptography Challenges List

Difficulty: Easy?
Category: Cryptography
Flag: GENCTF{Rh1n0_b@k1ng_Cha11}
Description When discovered they will be provided with a zip file. The zip file contains 1 folder (Baking) and the folder contains 3 files: Cyber bakery job request.pdf, bakedGood.txt.gpg, bakedHint.txt. Most of the hints are found in Cyber bakery job request.pdf and the flag is inside of bakedGood.txt.gpg. To open the bakedGood file the pdf file provided a hint to the password. Once in the bakedGood.txt.gpg file they will need to use a tool like gpg to decrypt it(Password is the same). Inside of the bakedGood file will then be a recipe and an encrypted flag. If they want to uncover the flag they will need to baked the flag in reverse in cyberchef. Once they do that the flag will be presented: GENCTF{Rh1n0_b@k1ng_Cha11}

Recipe:
		Take the 25 pounds of armored unicorn and place it gently into a large baking pan.
		Once all 25 pounds have been added to the baking pan slowly start adding the rest of the ingedients in order:
		1) 2 Tbsp of Charcode delimiter space base 16
		2) 1 Tbsp 64 RFC 4648
		3) 1 Tbsp base64 standard XOR binary 52
		Lastly) Bake

Recipe in reverse: 
    XOR
      -Key: 00110100
      -Scheme: Standard
      -Null preserving off
    from Base64
      -A-Za-z0-9+/=
      -Remove non-alphabet chars on
      -Strict mode off
    -From Charcode
      -Delimiter: Space
      -Base: 16
    -From Charcode
      -Delimiter: Space
      -Base: 16

Result: GENCTF{Rh1n0_b@k1ng_Cha11}
