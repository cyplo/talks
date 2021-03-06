# change slide !

# warmup game
volunteer[s] + 
* group : guess number of data transactions - protected and not
* sweet for guesses, sweet for volunteer

# (examples)
* car keys
* garage keys
* immobilizers
* public transport network info
* mobile phone network
* internet

# (examples) motivation for the talk
* so ubiqutous yet misundesrtood
* I'm not an expert, nor poperly math-skilled but can provide points to start learning
* field is so huge it was very hard for me to choose what to talk about

# (history) -> (subsitution)
* Ceasar's cipher

# quiz: any problems with this ?
* problems with substitution ciphers - guesses?
* problem1: prone to statistical analysis
* problem2: no message integrity heck
* problem3: no sender verification

# (polyalphabetic ciphers)
* a try to disguise the letter frequency
* enigma

# (one time pads):
* XOR plain letter with key letter
* one time pads: proved unreakable by Shannon, if the key is secret and random and as long as plaintext

# quiz: problems with all the stuff so far ?
* shared secrets are needed

# (symmetric crypt nowadays):
* reason for being called symmetric 

* stream ciphers
stream ciphers: plaintext stream XOR keystream
stream ciphers: used in 'realtime', ciper a bit, send, decipher [synchronous stream ciphers]
stream ciphers: infamous example: RC4


# (block ciphers)
generally accept a block and a key
some function and its inverse
naive: take a plaintext, divide into blocks, cipher, concat 
# quiz: what is the problem with that approach ?
* (show penguin)
* in fact it's easy to spot patterns, that's what the brain is for
* TV static: cosmic radiation

# quiz: what you can derive about the message from the ciphertext, even if the randomization is done properly ?
length

# quiz: other attacks ?


more modern: take a randomization of the plaintext, embed initialization vector in the first block, then embed a derivate in the second block etc

Data Encryption Stndard and then Advanced Enryption Standard

mostly side channel attacks, some theoretical attacks
'break' - anything better than bruteforcing key

performance: 700MB/s per execution thread on modern CPUs


#assymetric crypto
* say hi to alice and bob !
* a bit of history on the names, more names
* Eve, Mallory/Trudy, Wendy

while symmetric crypto is good for data at rest problems, or the same person using the data as encrypting it
it's not very good when it comes tokey exchange stuff

hence assymetric crypto
public key - allows checking signatures and encrypting
privatekey - signing and decrypting

# RSA as an example of public key crypto
oldest

Rivest, Shamir and Adleman

key generation:
* choose 2 primes at random: p and q
* n=pq
* derive public key from n, derive private key from n

# quiz: attacks/flaws ?
* insecure when not padded randomly
* bad randomness allows for key collisions
* google for private keys ;)
* private key security
* side channel attacks
* how to prevent most side channel attacks ? don't use key material for branching decisions


# part1: takeways:
* entropy is king
* most attacks are not the attacks on the math
* modern motivations: mostly privacy of the individual

# break


# let us deconstruct some protocols
* it's easiest to read info on https sessions, can we start with that ?

# https
* how to read the browser info
* first of all: is this the same info ?
* bit number differ, camellia ?

#quiz - ssl vs tls ?


* to wikipedia !
# TLS
Transport Layer Security (TLS) and its predecessor, Secure Sockets Layer (SSL), are cryptographic protocols which are designed to provide communication security over the Internet.[1] They use X.509 certificates and hence asymmetric cryptography to assure the counterparty whom they are talking with, and to exchange a symmetric key. This session key is then used to encrypt data flowing between the parties. 


* RSA
* 256
* CBC - cipher block chaining - block cipher mode
* SHA - cryptographic hash
* DHE

mention MAC - mac(key, message) = "tag" 

* TLS 1.2
* AES_128_
* GCM  - mode of operation 
* DHE_RSA key exchange

* there is an upgrade to existing plaintext connections: STARTTLS, maintain tcp connection

# (how to test implementations
* make a threat model
* don't implement on your own !
* check for information leaks - look at Tor project
* wireshark, cookies
* decouple network security from app security - insecure, duh !
* external audits

# notes on implementation
implementing - use libraries and understood designs because it's hard any other way
* don't use generic string comparison functions - timing attacks
* don't implement your own crypto

# quick review of attacks on attacks
# quiz: who said that: "properly implemented strong crypto still works"
* most of attacks - side channel ones

takeaways:
* strong crypto works
* random number generators are important
* never implement crypto systems from scratch


learn more about crypto
* https://www.coursera.org/course/crypto
* https://www.schneier.com/book-applied.html
* http://blog.existentialize.com/so-you-want-to-crypto.html

CCC: 

'this year in crypto'
* https://www.youtube.com/watch?v=HJB1mYEZPPA

side channel attacks
* https://www.youtube.com/watch?v=H-cpm7D8Sqg

and other stuff
* https://www.youtube.com/watch?v=CNXl56HuJaE

