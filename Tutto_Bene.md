# Tutto Bene
![image](https://github.com/user-attachments/assets/c429309d-d31e-46d0-bf3a-ba6ba541426a)


## Category: Cryptography  
**Author**: spicy-mochi

---

## Challenge Summary

This challenge involved a hash analysis problem using **SHA-512**. We were given a hash `h` and needed to reverse it by identifying matching 2-character pairs that were used to generate it.

The goal was to find the correct 2-character chunks that, when hashed and post-processed, matched substrings of `h`. These pairs were then used to reconstruct the flag.

---

## Step-by-Step Breakdown

### Step 1: Brute-force all 2-character pairs

- Generate all combinations of printable ASCII characters.
- For each pair:
  - Compute its **SHA-512 hash**
  - Extract multiple substrings from the hash digest
  - Reverse each substring
  - Store each reversed substring as a key and the 2-character pair as the value

This creates a lookup dictionary mapping hash segments to the original character pairs.

---

### Step 2: Slide a window over the target hash

- Slide a window over the target hash `h` and extract segments of the same size used earlier
- Reverse each segment and look up matching pairs from the dictionary
- Collect and store all valid pairs

---

### Step 3: Reconstruct the flag

- Once all valid pairs are identified, sort them based on their position in the hash
- Concatenate the pairs in order to form the full plaintext
- Clean up or manually adjust if anything looks off

> The final reconstruction required some **manual tweaking** to correct inaccuracies and get the exact flag.

---

## Script

![image](https://github.com/user-attachments/assets/98bdeb09-15b6-4537-a000-c398f9b47da0)


---

## The Flag

The output was not 100% accurate, so I manually adjusted to get the correct flag.

![image](https://github.com/user-attachments/assets/3118fa98-40c2-4def-97db-a7391730ccda)

