# Hashcat

## Sumarry of [Schneier 2015: Applied Cryptography](https://learning.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/10_chap02.html#chap02)

### [2.3 ONE-WAY FUNCTIONS](https://learning.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/10_chap02.html#chap02-sec003)

* A one-way function is a mathematical function that is easy to compute in one direction but significantly difficult to reverse.
* In cryptographic terms, given an input x, it is easy to compute the function f(x), but given f(x), it is computationally hard to find x.
* Although there is no mathematical proof of the existence of one-way functions, many functions behave like one-way functions, providing a foundation for cryptographic protocols.
* A trapdoor one-way function is a special type of one-way function that includes a secret trapdoor, which allows for reversing the computation under certain conditions.
* Easy to compute in one direction, hard to reverse but with knowledge of the secret (trapdoor), reversal becomes easy to compute.
* Trapdoor one-way function is used in public-key cryptography for secure communication.

### [2.4 ONE-WAY HASH FUNCTIONS](https://learning.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/10_chap02.html#chap02-sec004)

* Also known as compression function, contraction function, message digest, fingerprint, cryptographic checksum, message integrity check (MIC), and manipulation detection code (MDC).
* These functions convert variable-length input (pre-image) into a fixed-length output (hash value), serving as a fingerprint for the pre-image.
* Should be collision-free: hard to generate two pre-images with the same hash value.
* Publicly known; security relies on one-wayness and the difficulty of generating a matching pre-image.
* A single bit change in the pre-image changes, on average, half of the bits in the hash value.
* Used in file verification to prevent unauthorized changes and also, recipients can verify the hash without the need for a key.
* Message Authentication Codes (MAC) is a one-way hash function with the addition of a secret key.
* MAC has similar theory to hash functions, but only someone with the key can verify the hash value.
* MAC cryptographic mechanism provides a layer of confidentiality, allowing parties with the secret key to authenticate the origin and integrity of the message or data.

