# MSB
## Challenge Description
_This image passes LSB statistical analysis, but we can't help but think there must be something to the visual artifacts present in this image..._
## Walkthrough
We use stegsolve to decode our flag.  
Open the given image file in stegsolve and under `analyse` -> `data extract`.  
Since the data is hidden in **MSB(Most Significant Bit)** We start by checking all RGB boxes for 7 since it's the most significant bit  
<img width="1440" alt="Screenshot 2025-06-20 at 6 14 01 PM" src="https://github.com/user-attachments/assets/cbd37fbd-ae35-42f5-af6f-65d18a331099" />  
and under preview we see some plain text. So we save it to a `.txt` file and use `grep` command to extract the flag.
## Flag 
**picoCTF{15_y0ur_que57_ qu1x071c_0r_h3r01c_ee3cb4d8}**
