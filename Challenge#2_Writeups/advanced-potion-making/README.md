# advanced-potion-making
## Challenge Description
_Ron just found his own copy of advanced potion making, but its been corrupted by some kind of spell. Help him recover it!_
## Walkthrough
So we've got a file that has been corructed. Let's use a hex editor to analyse it. Since there is IHDR information in the header it's most likely a `PNG` file, but the signature appears to be faulty.  
We compare are file with a not corrupt png image file and make the following changes in the header-  
`42 11` -> `4E 47`  
`12 13 14` -> `00 00 0D`  
Now that we've fixed the file, we can save with `.png` extension and view it. It is an all red image.  
So we open paint and change the background colour of the image and we see the flag written in red.  
  
<img width="1375" alt="Screenshot 2025-06-19 at 8 40 56 PM" src="https://github.com/user-attachments/assets/8f364854-879f-4884-a12d-2ffb68aa8a70" />  

## Flag
**picoCTF{w1z4rdry}**
