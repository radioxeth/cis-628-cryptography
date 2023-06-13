# Week 6 Signatures, MACs, Secret Sharing, and Key Management

## Directory

## Live Session

### DES is a block cipher
56bit key

DES does not use a keystream

https://en.wikipedia.org/wiki/Horst_Feistel
1. multiple rounds of the same operations
2. half of data is encrypted 

DES is feistel

AES is SPN

f function is like a PRNG

E (Expansion) adds to diffusion and helps with cryptography


# Midterm Study List
- X Symmetric encryption vs. asymmetric encryption
- X Obsolete algorithms vs. current algorithms (for both hashing and encryption)
- X Terms (key, ciphertext, plaintext, algorithm, etc)
- X How PGP works
- X How TLS works
- X Digital signature
- X Digital certificate
- X When private keys and public keys are used
- Stream vs. block ciphers
- X How confidentiality and integrity are accomplished
- X Encryption vs. hashing
- Substitution cipher (algorithm, attacks)
- TRNG, PRNG, CSPRNG, OTP
- mod 2 addition, XOR
- Cryptology, cryptography, cryptanalysis

## The first 27 questions (2.5 points each) are multiple choice. The last 6 (4-6 points each) are applied questions that require you to:
- Decrypt ciphertext that was encrypted with the XOR cipher (no key provided)
- Decrypt ciphertext that was encrypted with the shift cipher (no key provided)
- Decrypt ciphertext that was encrypted with the substitution cipher (no key provided)
- Generate stream bits for an LFSR
- Compute using equivalence classes
- Find the modular multiplicative inverseSymmetric encryption vs. asymmetric encryption

### DES Continued/AES

Fiestel network inside DES box

What if we double encrypt with DES?

keyspace of 3 des is that which 2 des should be, 2^112

keyspace des  2^56
keyspace 2des 2^57
keyspace 3des 2^112

Given a block cipher with a key loength of k bits and block size of n bits as well as t plaintext-ciphertext pairs (x1,x1)


If the key size is greater than the block size, there will be dublicate keys