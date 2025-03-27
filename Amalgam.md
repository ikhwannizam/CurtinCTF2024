# Amalgam
![image](https://github.com/user-attachments/assets/66c62696-83cb-4f44-9d1c-ea830a757bfa)

## Category: Cryptography  
**Author**: spicy-mochi

---

## Challenge Summary

We are given an ElGamal-encrypted message, with the following values:

- `p`: A large prime modulus  
- `g`: Generator  
- `h`: Public key, computed as `h = g^x mod p`, where `x` is the private key  
- `c1`, `c2`: Ciphertext components  

Our goal is to **decrypt the ciphertext** and recover the flag.

---

## Step-by-Step Breakdown

### Understand ElGamal Encryption

ElGamal encryption works like this:

- Public key: `(p, g, h)` where `h = g^x mod p`
- To encrypt a message `m`:
  - Choose random `k`
  - Compute `c1 = g^k mod p`
  - Compute `c2 = m * h^k mod p`
- The ciphertext is `(c1, c2)`

To decrypt:
- Compute `s = c1^x mod p` (shared secret)
- Compute `s_inv = modular inverse of s mod p`
- Recover plaintext: `m = (c2 * s_inv) mod p`

So we need `x` (the private key) to decrypt. But we are only given `h = g^x mod p`, so we need to recover `x`.

---

## Decryption Script

This is the working decryption script:

![image](https://github.com/user-attachments/assets/61081186-dada-4c38-9dc8-c3075f675a0d)

---

## The Flag

![image](https://github.com/user-attachments/assets/59ec03ff-648e-4029-812d-a13a3ef188fb)

```text
CURTIN_CTF{dlP_50lv3d:)}
