![image](https://github.com/user-attachments/assets/02c34352-1cd4-407e-a392-65cb5f73bfdd)

By assuming the flag format would appear somewhere in the plaintext, I was able to:
- XOR the ciphertext against known portions of the expected flag prefix
- Try to derive the repeating key (if applicable)
- Reuse that key to decrypt the full ciphertext

This method is often referred to as **crib dragging** — where you use a “known plaintext” to work backward and discover the key.

For this example the known key is the flag format which is "CURTIN_CTF{"

this is the working decryption script:
![image](https://github.com/user-attachments/assets/fc679db3-1f30-440d-9c54-ae70e9ac0661)

the flag:

![image](https://github.com/user-attachments/assets/4a3bd3e1-d3fa-4637-9011-ba2ff3fe1534)
