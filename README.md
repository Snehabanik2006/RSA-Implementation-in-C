# RSA-Implementation-in-C
 

RSA in C

An educational implementation of the RSA written entirely in C without using external cryptographic or big integer libraries.

How It Works

The program implements RSA from scratch using custom arbitrary-precision integer arithmetic.

Key Generation

1. Generate two random prime numbers p and q using the Miller–Rabin primality test.
2. Compute:
   - n = p × q
   - φ(n) = (p − 1)(q − 1)
3. Choose the public exponent:
   - e = 65537
4. Compute the private exponent:
   - d = e⁻¹ mod φ(n)
5. The public key is (n, e) and the private key is (d).

Encryption

Given a message "m", the ciphertext is computed as:

c = m^e mod n

using modular exponentiation.

Decryption

The original message is recovered using:

m = c^d mod n

Features

- Custom Big Integer implementation
- Addition, subtraction, multiplication, and division
- Miller–Rabin primality testing
- Modular exponentiation
- Modular inverse computation
- RSA key generation
- RSA encryption and decryption

How to Compile

gcc rsa.c -o rsa

How to Run

./rsa

The program will:

1. Generate RSA keys.
2. Display the public and private key components.
3. Ask for a message.
4. Encrypt the message.
5. Decrypt the ciphertext.
6. Display the recovered plaintext.

Notes

- This project was developed for educational purposes and as part of a Cryptography Internship.
- The implementation focuses on understanding RSA and big integer arithmetic rather than performance.
- Large key sizes may require significant computation time due to the custom arithmetic routines.

Acknowledgements

Developed during a Cryptography Internship under the guidance of Dr. Subhabrata Samajder and Dr. Avik Chakraborty.

Disclaimer

This implementation is intended for learning and experimentation and should not be used for production cryptographic applications.