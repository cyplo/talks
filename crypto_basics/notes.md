# warmup game

volunteer[s] + 
* group : guess number of data transactions - protected and not

# examples
* car keys
* garage keys
* immobilizers
* public transport network info
* mobile phone network
* internet

# motivation for the talk
* so ubiqutous yet misundesrtood
* no master, but can provide points to start learning

# history
* Ceasar's cipher
* other substution ciphers - e.g. enigma
* some math(key, text) - code books
* one time pads
* problem: key exchange

# let us deconstruct some protocols
* with which do you want to start ?
* it's easiest to read info on https sessions, can we start with that ?

# https
* how to read the browser info
* first of all: is this the same info ?
* bit number differ, camellia ?

# TLS
Transport Layer Security (TLS) and its predecessor, Secure Sockets Layer (SSL), are cryptographic protocols which are designed to provide communication security over the Internet.[1] They use X.509 certificates and hence asymmetric cryptography to assure the counterparty whom they are talking with, and to exchange a symmetric key. This session key is then used to encrypt data flowing between the parties. 


* DHE
* RSA
* 256
* CBC
* SHA

* TLS 1.2
* AES_128_GCM - encrypted and authenticated
* DHE_RSA key exchange


* to wikipedia !
In cryptography, Camellia is a 128-bit symmetric-key block cipher jointly developed by Mitsubishi and NTT of Japan. The cipher has been approved for use by the ISO/IEC, the European Union's NESSIE project and the Japanese CRYPTREC project. The cipher has security levels and processing abilities comparable to the Advanced Encryption Standard.[1]

Camellia's block size is 16 bytes (128 bits), and can use 128-bit, 192-bit or 256-bit keys. The block cipher was designed to be suitable for both software and hardware implementations, from low-cost smart cards to high-speed network systems.[2]




# motivation for encrypting
* privacy - medical records

# history
* ceasar's cipher - sweet for [rot13]
*

implementing - use libraries and understood designs because it's hard any other way
* don't use generic string comparison functions - timing attacks
*

quick on attacks:
* "properly implemented strong crypto still works"
* most of attacks - side channel ones

don't implement your own crypto
* http://blog.existentialize.com/so-you-want-to-crypto.html

learn more about crypto
* https://www.coursera.org/course/crypto
* https://www.schneier.com/book-applied.html


