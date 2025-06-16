# Matryoshka Doll
## Challenge Description
_Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one?_
## Walkthrough
We have been given the file dolls.jpg attached here.  
Since we are looking for something placed _inside this file_ as deduced by the challenge description, we use the `binwalk` command to look for any embedded files.
```bash
binwalk dolls.jpg
```
From the output of binwalk command we see that there is a zip archive file embedded in our problem file.  
Use `-e` option with the `binwalk` command to extract embedded files.
```bash
binwalk -e dolls.jpg
```
The files are extracted in a directory called **dolls.jpg.extracted** inside the **extractions** directory just created. Use `cd` command to enter the directory.  
Now check the contents of the directory using the `-l` option with the `ls` command to get detailed description of enclosed files and directories.
```bash
$ ls -l
drwxr-xr-x  3 navyaagarwal  staff  96 16 Jun 20:27 4286C
```
The **'d'** before the permissions means that it is a directory. Use `cd` command to enter the directory. Use `ls -l` command again to check it's contents.  
This directory contains another called **base_images**, enter the directory and use `ls -l` command again. This directory contains another image file.  
We use the `binwalk` command on this file to find embedded zip archive file.

After repeating this process a number of times we land upon a file called **flag.txt**. Read the file using-
```bash
cat flag.txt
```
## Flag
**picoCTF{96fac089316e094d41ea046900197662}**
