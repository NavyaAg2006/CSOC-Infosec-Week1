# Information
## Challenge Description
_Files can always be changed in a secret way. Can you find the flag?_
## Walkthrough
We have been given the image file attached.  
First we use the `file` command to check the file type.
```bash
$ file cat.jpg
cat.jpg: JPEG image data, JFIF standard 1.02, aspect ratio, density 1x1, segment length 16, baseline, precision 8, 2560x1598, components 3
```
File already has the correct extension.
> [!NOTE]
> The first hint of the challenge is:-  
> Look at the details of the file
We use the `exiftool` command to look at the details of the file.
```bash
exiftool cat.jpg
```
from the results the license appears to be encoded data. We copy it and try base 64 decoding.
```bash
$ echo "cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9" | base64 -d
picoCTF{the_m3tadata_1s_modified}
```
The flag is found.
## Flag
**picoCTF{the_m3tadata_1s_modified}**
