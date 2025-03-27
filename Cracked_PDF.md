# Cracked PDF
![image](https://github.com/user-attachments/assets/c8067d21-8832-4cbe-92d9-469f1a45da3e)

---

## Challenge Summary

This challenge involved a password-protected PDF that contained hidden content beneath the surface. The process required both password cracking and some light steganographic inspection to extract the flag.

---

## Step-by-Step Breakdown

### Step 1: Crack the PDF Password

Used `pdf2john` and `john` to recover the password.

```bash
pdf2john.py target.pdf > hash.txt
john hash.txt --wordlist=rockyou.txt
```

## The recovered password

```bash
PRETTY
```
---

###  Step 2: Inspect the PDF

-Opened the PDF using PDF XChange Editor
-Selected all visible and non-visible elements
-Discovered hidden text layered under the visible content
-Copied the hidden data into a text file or code editor

![image](https://github.com/user-attachments/assets/e4e15e24-a152-469a-ad84-b1e2a361ce63)

![image](https://github.com/user-attachments/assets/15a1ba52-20f7-4c09-8fb3-ccf4793993d8)


### Step 3: Decode the Obfuscated Flag

The hidden text found in the PDF consisted of two characters: `_` and `.`. These represented binary data:

- `_` → `1`  
- `.` → `0`

To decode it:

1. Replace all `_` with `1` and `.` with `0` using a simple Python script:

```python
binary = encoded_text.replace('_', '1').replace('.', '0')
```

![image](https://github.com/user-attachments/assets/a4fde753-d8be-4824-88af-858d8dcad2ab)


Take the resulting binary string and convert it to ASCII using CyberChef

![image](https://github.com/user-attachments/assets/e3bf209a-4e31-4548-918e-f0b8b7540b21)

