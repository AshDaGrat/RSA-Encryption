# RSA-Encryption

Cryptography is the practice and study of techniques for secure communication in the presence of adversarial behaviour. More specifically it is the process of obfuscating and deobfuscating data using certain cryptographic techniques. 

The way this obfuscation was initially done required the two parties to meet up in person and exchange a secret key. This same key would be used to obfuscate the data by both parties and thus was referred to as a symmetric key system. This system was obviously inefficient since it was not always possible to arrange an in person meetup, and sending the secret key over an unsecured channel means anyone can decrypt your messages. 

However in 1977 Ron Rivest, Adi Shamir and Leonard Adleman developed RSA encryption. An asymmetric key distribution system, where everyone has access to what is known as a “public key” and can use it to encrypt messages. But only the party to whom the message is destined has access to the “private key” to decrypt messages. 

# How does RSA work?

1. The first step in RSA encryption is to select two large primes, p and q. This is usually done by just generating a random number then performing the Rabin-Miller primality test. Typically the primes selected are 1024 to 2048 bits long. 

2. We then compute the product of these two primes, denoted by n.  

3. We also compute the Euler Totient function (n) = (p-1)(q-1)

4. We then select a random small off integer that is co-prime to (n) 

5. Finally we compute d, the multiplicative inverse of e modulo (n)

6. Our RSA public key is P = (e,n) and our secret key is S = (d,n)
