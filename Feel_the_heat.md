# Feel The Heat
![image](https://github.com/user-attachments/assets/cefe1329-388f-4883-a218-4da271521833)

## Category: Cryptography  
**Author**: spicy-mochi

---

## Challenge Summary

This challenge required decrypting a message that had been encrypted using a **partial differential equation (PDE)**-based approach — something not very common in typical CTFs.

There were two parts to the decryption:

1. **Key Decryption**  
   - A key file (`decrypted_key`) was given, and we needed to recover the original AES key from it.
   - The key was padded, so we had to remove padding properly to extract the valid key.

2. **Flag Decryption via PDE Reversal**  
   - The encryption used a 1D heat diffusion model to transform the original message.
   - We needed to **reverse the heat diffusion** over time to recover the plaintext flag.

---

## Step-by-Step Breakdown

### Part 1: Recover the AES Key

- Load the encrypted key.
- Use AES decryption with the known key and IV.
- Apply `unpad()` to remove PKCS7 padding.
- Handle exceptions to ensure clean recovery.

### Part 2: PDE-Based Flag Recovery

- Define the PDE function (heat equation) used during encryption.
- Use `odeint` from `scipy.integrate` to **solve the equation backward in time**.
- Use the decrypted AES key as the diffusion coefficient `k`.
- The result at `t=0` should approximate the original message.
- Convert the final values into characters by rounding to the nearest ASCII integer and joining the characters.

---

## Solving using PDE backwards in time.

![image](https://github.com/user-attachments/assets/5bd94fef-c622-4bca-a32b-396246cc30f8)

![image](https://github.com/user-attachments/assets/8fec14c7-3796-4ec9-91c1-a9fb0af74740)


---
## The Decryption script

![image](https://github.com/user-attachments/assets/4deb0f5a-6ab2-4c29-b11e-73a2fdbcc5ae)



## The Flag

![image](https://github.com/user-attachments/assets/5e73ca8a-9f74-431e-a212-65e668b49ca6)

