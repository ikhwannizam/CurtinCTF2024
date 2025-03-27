# Trivial 1
![image](https://github.com/user-attachments/assets/03f5b4b5-d114-49fb-9930-62dc24ef6050)

---

## Challenge Summary

The challenge seemed to involve identifying a number-based flag, potentially involving prime numbers. Given the limited range (1 to 100), a brute-force approach was practical.

I wrote a simple script that iterated through all integers from 1 to 100 and checked whether each number was prime. For each prime number (and also for some non-primes for completeness), I formatted it in the expected flag format and submitted it until I found the correct one.

This technique works well when:

- The flag is based on a mathematical property (like primality)
- The input space is small (1–100)

---

## Script

This is the working code:

![image](https://github.com/user-attachments/assets/854f166a-67d6-4c2a-91f0-15bd91a20a32)

---

## The Flag

![image](https://github.com/user-attachments/assets/ef8a1824-722b-4ea8-a095-a7474dc1357a)

```text
CURTIN_CTF{...}
