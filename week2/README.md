# Week 2 More on Classic Ciphers and Their Math

## Directory
- [Home](/README.md#table-of-contents)
- [Week 1 Introduction to Cryptography](/week1/README.md#directory)
- **&rarr;[Week 2 More on Classic Ciphers and Their Math](/week2/README.md#directory)**
- [Week 3 Modern Block Ciphers and a Start on RSA](/week3/README.md#directory)

## Live Session

Continued from last week

PGP (Pretty good Privacy)

- encrypt email with a symmetric session key
- recipient sends the public key
- encrypt encrypted emial with recipient's public key
- receive both messages
  - open with their private key
  - uses symmetric key to decrypt the message.


### best of both worlds
- symmetric key cryptography for the speed
- assymmetric key cryptography for the security

### Certificate Authority

- gives out digital certificates
  - signed by CA
  - certificates have public key for the server

### How TLS 1.2 Worked

1. clientHello
   - 
2. serverHello
3. ClientKeyExchange

### Hashing
- for: integrity
  - messages
  - file transfers


messages->hash function->hash (message digest)

- characterstics
  - chagning a single bit of the hash drastically changes the output
  - variable length input, fixed length output
  - perimage resistance
    - given a hash value h it should be difficult to find any message m such that h=hash(m). This concept is related to that of a one-way function
  - second preimage resistance
    - given an input m1, it should be difficult to find a different input m2 such that hash(m1)=hash(m2). This property is sometimes referred to as weak collision resistance. Funcitons that lack this property are vulnerable to second-preimage attacks.
  - Collision resistance
    - it should be difficult to find two different messages m1 and m2 such that hash(m1)=hash(m2). Such a pair is called a cryptographic hash collision.

### Two types of collission attacks

- classic collision attack
  - mathematically stated, a collision attack finds two different messages m1 and m2, such that hash(m1)=hash(m2). in a classical collision attachk, the attacker has no control over the content of either message, but they are arbitrarily chosed by the algorithm

- chosen-prefix collision attack
  - an extentsion of the collision attack is the chosen-prefix collision attack, which is specific to merkle-damgard hash functions. In this case, the attacker can hoose two arbitrarily different documents, and then append different calculated values that result in the whole documents having an equal hash value. This attack is much more powerful thatn a classical collision attack.
  - 

### Hashing

- also for confidentiality of password databases
- obsolete hash functions: MD5 SHA-1
- today's standard hash functions/algorithms: SHA-2, SHA-256, SHA-512, SHA-3
  - except for password databases
    - PBKDF2
    - bcrypt
    - scrypt
    - Argon2
    - yescrypt

> Password databases are never encrypted. They are hashed.

### Attacks on Password Hashes

- brute force attack
- dictionary attack
- rainbow table attack


### Certificate Authority
- CA encrypts the hash with their private key
  - this is a digital signature

- Browser recieves digitially signed data
  - decrypts the data with the CA's public key
    - root browser certificate store

### Certificate Types

- Domain Validation
- Organizaiton Validation
- Extended Validation

### Revocation Methods
- CRL (Certificate Revocation List)
- OCSP (Onlice Certificate Status Protocol)