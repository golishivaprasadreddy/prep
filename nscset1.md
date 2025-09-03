1. Classify different types of security attacks (with examples)

Security attacks are broadly classified into Passive and Active attacks.

🔹 Passive Attacks (just observe, no modification)

Eavesdropping (Interception): Attacker listens to communication.
Example: Sniffing packets over Wi-Fi to steal passwords.

Traffic Analysis: Observing communication patterns.
Example: Even if encrypted, attacker notices frequent messages between two spies.


🔹 Active Attacks (modify, disrupt, or fabricate data)

Masquerade (Impersonation): Attacker pretends to be a valid user.
Example: Phishing login pages.

Replay Attack: Capturing valid data and resending later.
Example: Reusing a banking transaction request.

Modification of Messages: Changing data in transit.
Example: Altering “Amount = 1000” to “Amount = 10000.”

Denial of Service (DoS): Overloading a system.
Example: Flooding a server with requests.



---

2. Substitution and Transposition Encryption Example

Message: HELLO

Substitution (Caesar Cipher, shift = 3)

H → K

E → H

L → O

L → O

O → R
Ciphertext = KHOOR


Transposition (Rail Fence Cipher, depth = 2)

Write diagonally in 2 rows:

H   L   O  
 E L

Read row-wise → HLOEL

So final:

Substitution result: KHOOR

Transposition result: HLOEL



---

3. Compare RSA with another asymmetric cipher

RSA (Rivest–Shamir–Adleman)

Encryption: 

Decryption: 

Relies on difficulty of factoring large primes.

Example:

Public key: (e=7, n=33)

Private key: (d=3, n=33)

Encrypt: M=4 → C = 

Decrypt:  ✅



ElGamal Cipher

Based on Discrete Logarithm Problem.

Uses randomization in encryption → produces different ciphertexts for same plaintext.

Stronger against chosen-plaintext attacks.


Comparison:

RSA: deterministic, easier key management.

ElGamal: probabilistic, stronger security but longer ciphertext.



---

4. Block Cipher Operation Modes

A block cipher (like AES) can be used in different modes:

ECB (Electronic Code Book):
Each block encrypted independently.

Pros: Simple.

Cons: Same plaintext → same ciphertext (patterns visible).


CBC (Cipher Block Chaining):
Each block XORed with previous ciphertext.

Pros: Hides patterns.

Cons: Error in one block affects current and next block.


CFB (Cipher Feedback):
Converts block cipher into stream cipher.

Good for real-time data.


OFB (Output Feedback):
Like CFB but error does not propagate.

CTR (Counter Mode):
Uses counters and parallel encryption.

Pros: Fast, parallelizable.

Cons: Reusing counter = fatal.




---

5. Digital Signature Scheme – Authentication & Integrity

Steps:

1. Sender computes hash of message (H(M)).


2. Encrypts hash with private key → digital signature.


3. Sends Message + Signature.


4. Receiver decrypts signature with sender’s public key and compares with H(M).



✔ Proves Authentication (only sender has private key).
✔ Proves Integrity (any change → hash mismatch).

Example:

Message = "Pay 1000"

Hash = 12345

Sender signs hash with private key → Signature = 67890

Receiver verifies with public key → confirms authenticity.



---

6. Message Authentication Methods

Ways to authenticate messages:

1. Message Authentication Code (MAC):
Uses secret key + message → fixed-size code.



2. Hash Functions:
Hash message, send hash along. Receiver recomputes and checks.


3. Digital Signatures:
Encrypt hash with private key. Provides authentication + non-repudiation.


4. Hybrid (HMAC):
Combines hash + secret key → strong authentication.