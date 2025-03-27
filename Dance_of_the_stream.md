![image](https://github.com/user-attachments/assets/e3361e5f-4ccf-4b91-a13a-3051b2982080)

This challenge involved reversing a custom stream cipher encryption. We were given:

- A Python script implementing a stream cipher (with quarter-round operations)
- Two files: `ciphertext.txt` and `o_nonce.txt`
- The flag was hidden in the ciphertext, and the key was unknown (brute-force required)

Step-by-Step Breakdown:

Understand the Encryption Algorithm

The script uses a **custom stream cipher** (similar to ChaCha20), with the following characteristics:

- `q_r()` function implements quarter-round transformations using XOR, shifts, and addition.
- The `stream()` function builds a keystream block based on a key, nonce, and counter.
- `stream_e()` XORs the plaintext/ciphertext with the keystream.
- A function called `o_value()` obfuscates input values using a static byte-string (`b'leomessi'`).
- The `recover_nonce()` function reads and de-obfuscates a nonce value from `o_nonce.txt`.
- The decryption attempts all 16-bit keys (0x0000 to 0xFFFF) to recover the plaintext from the ciphertext.


Identify What Needs Brute-Forced

- The **nonce** is recovered using `o_value()` on the obfuscated nonce file.
- The **key** is unknown and must be brute-forced.
- The plaintext is considered valid only if it is fully printable ASCII.

the decryption code is too long to screenshot, so i include the script as a text file here.

[decrypt.txt](https://github.com/user-attachments/files/19492999/decrypt.txt)

the flag:
![image](https://github.com/user-attachments/assets/ce0c9f70-6ab3-4502-9d78-a963f38d3486)
