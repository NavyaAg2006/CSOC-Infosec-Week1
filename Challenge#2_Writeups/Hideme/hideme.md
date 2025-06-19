# Hideme
## Challenge Description
Every file gets a flag.  
The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye.  
## Walkthrough
We have been given a file called **Flag.png** on using the `binwalk` command we find an embedded zip archive file. Extract it using
```bash
binwalk -e Flag.png
```
We find the file `flag.png` inside `9B3B/secret/`
![flag](https://github.com/user-attachments/assets/68ef581f-16f8-4a15-ab3e-9e1abcc6a56b)
## Flag
**picoCTF{Hiddinng_An_imag3_within_@n_ima9e_cda72af0}**
