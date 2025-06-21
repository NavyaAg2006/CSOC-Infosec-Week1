# Extensions
## Challenge Description
_This is a really weird text file TXT? Can you find the flag?_
## Walkthrough
Use the `file` command on the file **flag.txt**, it will tell us that it's png image data. Change the file's extension to `.png` using
```bash
mv flag.txt flag.png
```
View the file using an image viewer.
## Flag
**picoCTF{now_you_know_about_extensions}**
