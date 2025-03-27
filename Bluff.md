# Bluff
![image](https://github.com/user-attachments/assets/02c34352-1cd4-407e-a392-65cb5f73bfdd)

---

## Challenge Summary

This challenge involved an XOR-encrypted ciphertext without any clear key.

By assuming the flag format would appear somewhere in the plaintext, I was able to:
- XOR the ciphertext against known portions of the expected flag prefix
- Try to derive the repeating key (if applicable)
- Reuse that key to decrypt the full ciphertext

This method is often referred to as **crib dragging** — where you use a “known plaintext” to work backward and discover the key.

In this case, the known plaintext was the flag prefix:

```text
CURTIN_CTF{
```

## This is the script
![image](https://github.com/user-attachments/assets/c8c71a96-35b1-4111-83f7-3da8fa3177e4)

## THe flag
![image](https://github.com/user-attachments/assets/7d9f0037-b04f-422f-9227-305a2bb9f565)

