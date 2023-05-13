# Week 5 Elliptic Curve Based Cryptosystems and Crypto Hash Functions

## Directory

## Live Session

### Problems with Computational Security

`rand()`

$S_0=seed$
$S_{i+1}\equiv{AS_i+B\mod{m}}, i=0,1,...$

Do not use a PRNG

### Multiple Solutions
in case $gcd((S_1-S_2),m)\neq{1}$

if we know a little bit of plaintext, we can figure out the rest

Building key streams from CSPRNGs

- linear feedback shift registers (LSFR)
  - one iteration is cryptographically weak
  - multiple is stronger
- A5/1 cipher

### Linear Feedback Shift Registers (LSFR)
- LSFR consist of clocked storage elements (flip-flops) and a feedback path.


- The input is only going to be measured when the clock is on an upswing

- A5/1, A5/2, bluetooth

## Data Encryption Standard (DES)

Claud Shannon
- Diffusion AND Confusion



## Midterm
**Midterm opens next week after live 6**
Review sheet