# securemsging-rsa
Consists of sender and receiver code for secure messaging using RSA

The code in the jupyter notebook file includes both sender and receiver source code.

The sender:

Digitally sign a message (file) using RSA PSS to produce a file called msg.sig.
Encrypt the message using AES with a 128 bit key K to produce a file called msg.crypt.
Encrypt K using RSA with the receiver's public key and save to a file called symkey.crypt.
"Transmit" msg.sig,msg.crypt,symkey.crypt

The receiver:

Uses their private key to decrypt symkey.crypt to produce symkey.
Uses symkey to decrypt msg.crypt to produce msg.
Uses the sender's public key to verify that msg.sig is a valid signature for msg.

