# Cryptography  
---
## Introdution 
#### The Shift (or Caesar) Cipher is another monoalphabetic substitution cipher. Although more secure than the Atbash Cipher, it is still an easy cipher to break, especially by today's standards. Originally, it was used by Julius Caesar for sending encrypted messages to his troops, as recorded by Suetonius:

#### This describes what we would now call a shift of 3, and describes the cipher that Caesar used quite well. That is, "a" was encrypted as "D", "b" as "E", etc. The table below gives the plaintext alphabet and the ciphertext alphabet to show how a shift of 3 could be depicted.

![](https://crypto.interactive-maths.com/uploads/1/1/3/4/11345755/190935_orig.jpg)
---

## Encryption
#### Encryption using the Shift Cipher is very easy. First we must create the ciphertext alphabet, which as discussed above is simply found by 'shifting' the alphabet to the left by the number of places given by the key. Thus a shift of 1 moves "A" to the end of the ciphertext alphabet, and "B" to the left one place into the first position. As the key gets bigger, the letters shift further along, until we get to a shift of 26, when "A" has found it's way back to the front. We have already seen a shift of 3 in  the table above, and below we have a shift of 15.

![](https://crypto.interactive-maths.com/uploads/1/1/3/4/11345755/5567092_orig.jpg)

#### Clearly, the encryption table and its inverse are the same as each other, only reordered. If we have received the ciphertext "PDUFXV EUXWXV", and we know that it has been enciphered using the key 3, then we can use the table to decipher the message. We see that  "P" represents the plaintext letter  "m",  "D" represents  "a" and so on. Continuing in this way we retrieve the plaintext  "marcus brutus", the name of the famous conspiritor in the assassination of Julius Caesar.

---
## Decryption
#### Decryption by the intended recipient of a ciphertext received that has been encrypted using the Shift Cipher is also very simple. One can either use the table already created above, and find each letter of the ciphertext in the bottom row, and replace with the corresponding plaintext letter directly above it, or the recipient could create the inverse table, with the ciphertext alphabet on top, and using a shift of -3 on it, which gives the table below.
![](https://crypto.interactive-maths.com/uploads/1/1/3/4/11345755/5906642_orig.jpg)

#### Clearly, the encryption table and its inverse are the same as each other, only reordered. If we have received the ciphertext "PDUFXV EUXWXV", and we know that it has been enciphered using the key 3, then we can use the table to decipher the message. We see that  "P" represents the plaintext letter  "m",  "D" represents  "a" and so on. Continuing in this way we retrieve the plaintext  "marcus brutus", the name of the famous conspiritor in the assassination of Julius Caesar.


![](https://blog.mdaemon.com/hs-fs/hubfs/Imported_Blog_Media/OpenPGPEncrypt-1.jpg?width=960&height=720&name=OpenPGPEncrypt-1.jpg)
