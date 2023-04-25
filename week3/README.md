# Week 3 Modern Block Ciphers and a Start on RSA

## Directory
- [Home](/README.md#table-of-contents)
- [Week 2 More on Classic Ciphers and Their Math](/week2/README.md#directory)
- **&rarr;[Week 3 Modern Block Ciphers and a Start on RSA](/week3/README.md#directory)**
- [Week 4 More on RSA](/week4/README.md#directory)

## Live Session

### Simple Symmetric Encryption:
The Substitution Cipher

> Historically, this type of cipher has been used many times, and it is a good illustration of basic cryptography. We will use the substitution cipher for learning some important facts about key lengths and about different ways of attacking ciphers

The idea is very simple: We substitute each letter of the alphabet with another one

>The goal of substitution cipher is the encryption of text, as opposed to bits in a modern digital system

**The substitution cipher is not secure at all!**
***
**Definition 1.2.1** Basic Exhaustive Key Search or Brute-force Attack

Let(x,y) denote the pair of plaintext and ciphertext, and let K={k1,..,kk} be the key space of all possible keys k_i. A brute force attack now cheks for every k_i&in;K if

d_ki(y)=K
***
How do we know what the plaintext is? *Compare to the header table*

Cipher-text is computationally secure against brute force attack - key space of the substituion cipher 26! .. ~2^88 (end of the universe lol)

- The major weakness of the cipher is that each plaintext symbol always maps to the same cipher text symbol.
  - that means that the statistical properties of the plaintext are preserved in the ciphertext
- look for frequent letters in the cipher text that appear frequently in plain text

*Second attack*: **Letter Frequency Attack**

Lessons learned
- good ciphers should hide the statistical properties of the encrypted plaintext
- the ciphertext symbols should appear to be random
- also, a large key space alone is not sufficient for strong encryption

### Implementation Attacks
- side-channel analysis can be used to obtain a secret key, for instance, by measuiring the electrical power consumption of a process which operates on the secret key
- em waves
- implementation attacks generally follow social engineering attacks

**Auguste Kerckhoffs**
https://en.wikipedia.org/wiki/Auguste_Kerckhoffs

Hiding the algorithm you use for encryption makes you less secure and more vulnerable
Hide the key

**Definition 1.3.1** Kerckhoffs Principle:
The principle holds that a cryptosystem should be secure, even if everything about the system, except the key, is public knowledge. This concept is widely embraced by cryptographers, in contrast to security through obscurity, which is not.


**How many Bits are enough?**
56-64 bits is good for few hours or days
112-128 bits several decades but not post quantum
256 bits is post quantum secure

### Why Modular Arithmetic for Crypto?
- can easily create groups, rings and fields, the fundamental buiding blocks of most modern public-key cryptosystems
- cryptography requires hard problems
- cryptography is implemented digitally, and works will if values can't be of arbitrary sizze.
- There are fixed lengths to data sets, size of data types in memory
- finite sets
- 
n=9
set {0,1,2,3,4,5,6,7,8}
8+4=12, 12/9=3 (4/3 but we don't care about the quotient, only the remainder)

(a-r)/m
(12-3)/9
9/9=1
no remainder



**Equivalence Class Table**

**Definition 1.4.2 Ring**

a+b=c mod m, c&in;Z_m
axb=d mod m, d&in;Z_m

> multiplicative inverse here means modular multiplicative inverse
a*a^-1 = 1 mod m



**Shift Cipher (Caeser Cipher)**
Definition 1.4.3 Shift Cipher
https://en.wikipedia.org/wiki/Caesar_cipher

ek(x)=x+k mod 26
dk(y)=y-k mod 26

**Aphine Cipher**
ek(x)=y=a*x+b mod 26
dk(y)=x=a^-1(y-b) mod 26

gcd(a,26)=1

a must be coprime with the modulus

**Possible midterm question**
write a 3 line python script to decrypt the shift ciper