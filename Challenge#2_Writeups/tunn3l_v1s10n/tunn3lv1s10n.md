# tunn3l v1s10n
## Challenge Description
_We found this file. Recover the flag._
## Walkthrough
So we have just been given a file and the challenge description doesn't say a lot so let's start by analysing the file.  
We start by using the `file` command to identify it's type but it outputs `data` so it's probably a corrupted file. We also use the `binwalk` command to see if there's any embedded files but there aren't.  
So we use a hex editor to analyse our file. The header starts with BM therefore it's a bitmap image file but it's corrupted.  

  
<img width="680" alt="Screenshot 2025-06-17 at 7 22 08 PM" src="https://github.com/user-attachments/assets/3031ded3-2618-4c42-b7cb-7dd32eed4d20" />
  
  
A few bits in the first row in the header spell BAD. These are clearly the corrupted bits so we compare it with a BMP file and replace those bits with constant values, now our file is not corrupted and can be viewed.

  
![a1](https://github.com/user-attachments/assets/37be10e5-45ef-42a7-8a55-8867f5ac1609)

  
The image seems to have a fake flag. But it seems to be a cropped image and also is a very weird dimension for an image so we use the `exiftool` command to look at the dimensions. The height of the image is 306 which seems to be very less so in our hex editor we find the bits representing 306 and change them to 1000.  
Now when we look at our image, we see the complete image with the flag.
![a4](https://github.com/user-attachments/assets/c6e0506f-aa6d-4eef-83be-b85cb999fc8f)

## Flag
**picoCTF{qu1t3_a_v13w_2020}**
