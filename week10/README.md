# Week 10 Quantum Cryptography and Computing, Post-Quantum  Crypto

## Directory

### Encryption and Decryption: Fast Exponentiation


### SAM Square and Multiply Algorithm

$x^{26}=x^{11010_2}=x^{(h_4h_3h_2h_1h_0)_2}$

Always start by squaring
If the next exponent is 1, multiply, otherwise square
0. $x=x^{1_2}$
1a. $x(^1)^2=x^2=x^{10_2}$
1b. $x^2x=x^3=x^{10_2}x^{1_2}$

skip half of th multiplicatoins on average


### Chinese remainder theorem

split mod n into mod p * mod q

### Diffie-Hellman Key Exchange
Key exchange algorithm, not an encryption algorithm

solves the key distribution problem

Diffie-Hellman Set-up

1. choose a large prime p
2. choose and exchange integer $\alph\in\{2,3,5,...,p-2\}$
3. 


Diffie-hellman uses private key for authentication
RSA uses public key to encrypt the premaster secret


OFB errors do no propagate
CFB errors do propagate

CTR can be done in parallel, no patterns, errors don't propagate

GCM Galois/Counter Mode
-> MAC Message Authentication Checksum
-> similar to digital signature

Digital signatures use asymmetric key cryptography
MACs use symmetric key cryptography

MACs do not provide nonrepudiation