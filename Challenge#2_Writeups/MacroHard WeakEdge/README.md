# MacroHard WeakEdge
## Challenge Description
_I've hidden a flag in this file. Can you find it?_
## Walkthrough
We have been given a powerpoint presentation file, let's start by viewing it. There seems to be nothing given in the presentation itself.  
Presentations are actually zip files so let's change the file extension to `.zip` and **unzip** the file.  
After analysing the contents we find file called `hidden` in the following path-
```bash
cd ppt/slideMasters
```
The text in the file appear to be base64 encoded, but there's spaces in between so we use this command to remove spaces then decode it.
```bash
cat hidden | tr -d ' ' | base64 -d
```
And we get the flag.
## Flag
**picoCTF{D1d_u_kn0w_ppts_r_z1p5}**
