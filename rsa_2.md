# RSA 2
![image](https://github.com/user-attachments/assets/aa2f4f8a-c36d-4382-ac0a-a1ec76e75ddc)

## Category: Cryptography  
**Author**: spicy-mochi

---

## Challenge Summary

This was a classic RSA challenge. The given information included:

- `n` — the RSA modulus, calculated as `n = p * q`
- `e` — the public exponent (typically 65537)
- `c` — the ciphertext (encrypted flag)

Our objective was to **decrypt the ciphertext** by recovering the private key `d` and using it to compute the plaintext.

---

## Step-by-Step Breakdown

### Step 1: Factor `n`

To decrypt RSA, we first need to factor the modulus `n` into its prime components `p` and `q`.

We used **RsaCtfTool**, which automates this process and supports multiple attack strategies.

```bash
python3 RsaCtfTool.py -n <modulus> -e <exponent> --uncipher <ciphertext>
```

![image](https://github.com/user-attachments/assets/e4148bce-0d43-4316-a65d-9debe1dec775)

## The output will the privavte key.

![image](https://github.com/user-attachments/assets/2fca3e38-f995-4fa0-8512-5be6fa9a6e0e)

## Step 2: Then we decrypt using this script:
![image](https://github.com/user-attachments/assets/d79939ed-fcbd-4666-b5d9-310b383192c4)

## The flag:

![image](https://github.com/user-attachments/assets/7b581356-b2e0-463c-a30f-f05bf195649d)




