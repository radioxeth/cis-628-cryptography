# Week 9 Security Models

## Directory


### Modular Multiplicative Inverse
Extended Euclidean Algorithm
EEA

&phi;(m) is the product of the primes is how many multiplicative inveres there are in a number

you're not doint &phi; unless you know what the primes are.
(Post quantum cryptography can derive the primes quickly, so RSA will die)

Prime factorization is the heart and sould of RSA
need 

> **Euler's Theorem**
> $a^{\phi{(m)}}\equiv{1\mod{m}}$

$\phi{(p)}=p^1-p^0=p-1$

$a^\phi{(p)}=a^{p-1}\equiv{1\mod{p}}$

### RSA and Diffie Hellman

Diffie Hellman is a key exchange protocol
RSA is an asymmetric key algorithm

RSA is several times slower than AES and other symmetric key encryption algorithms

$key(n,e)=k_{pub}$
$x^e\mod{n}$
$key\space{}d=k_{priv}$
$y^d\mod{n}$


#### RSA key generation
1. choose two large primes p and q
2. compute n=p*q (part of public key)
3. compute $\phi{(n)}=(p-1)(q-1)$
4. select the public exponent $e\in{\{1,2,...,\phi{(n)}-\}}$
such that $gcd(e,\phi{(n)})=1$
5. Compute the private key d such that 
$d*e\equiv{mod\phi{(n)}}$


e=3,17,$2^{16}-1$

1. p=3, q=11
2. n=p*q=33
3. $\phi{(n)}=(3-1)(11-1)=20$
4. choose e=3
5. $d\equiv{e^{-1}}\equiv{7\mod{20}}$


#### RSA encryption
k_pub=(33,3)
$y=x^e\equiv{}4^3\equiv{}31\mod{33}$
y=31

#### RSA decryption
$y^d=31^4\equiv{4}=x\mod{33}$

#### Why RSA is secure
if you have $\phi{(n)}$ you have the private key


### two distinct attacks on crypto systems
- analytical attacks try to break the algorithm
- implementation attack 


RSA REQUIRES PADDING
use OAEP