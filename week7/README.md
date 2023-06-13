# Week 7 E-Cash and Games

## Directory

## Advnaced Encryption Standard (AES)
- AES is most widely used symmetric cipher today
- AES is the standard both in NIST and industry
- To date, there are no better attacks better than brute-force known against AES
- AES will survive post quantum computing, unlike RSA, Diffie-Helman, eliptical curve, etc



## AES Standard
- block cipher with 128 bit block size
- three key lengths must be supported 128, 192, 256
- security
- efficiency in software and hardware

### AES
- should be good for several decades, even longer
- AES is the Rijndael cipher.
- key size dictates how many rounds you go through
- 256 bit key length 14 rounds
  - more rounds more diffusion
- in AES, all bits are encrypted in each round

### AES Algorithm
- no mixed column in the last round
- doesnt weaken the security and someone can easily nuke it

plaintext->key addition layer->byte substitution layer->ShiftRows and MixColumn layer (diffusion layer)->key addition layer->... n -> no mix column layer

- key addition layer
- byte substitution layer
  - s boxes
- diffusion layer
  - diffusion over all state bits
  - shift rows 
  - mix column


DES has 8 sboxes per round
AES has 16 sboxes per round

DES has 8 sboxes that are all different
AES has 16 sboxes that are the same

AES sboxes have several mathematical properties that DES does not have
you can use any sbox in 