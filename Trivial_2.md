![image](https://github.com/user-attachments/assets/56fe581f-65bc-4231-8930-be2ef02be6c0)


This challenge used a basic encryption method that applied a **polynomial-based transformation** to the original string (likely the flag). The encryption formula in the source or the given file hinted at a reversible transformation.

The core idea was to **reverse the transformation** using basic algebra or code. By analyzing how the encryption altered each character or number, I reconstructed the inverse logic — essentially decoding the polynomial function step-by-step.

This was done either by:
- Manually deducing the inverse formula
- Or writing a simple Python script to reverse it

this is the question encryption code:
![image](https://github.com/user-attachments/assets/f93a76c1-210c-44c4-b358-e07e9205e2a8)

this is my working decryption code:
![image](https://github.com/user-attachments/assets/503483f6-d5c7-454d-b531-40a042e32650)

the flag:
![image](https://github.com/user-attachments/assets/3c88d8fb-5cbc-41cb-80c4-6c3c3caa62e9)
