# File Types
## Challenge Description
_This file was found among some files marked confidential but my pdf reader cannot read it, maybe yours can._
## Walkthrough
This challenge requires us to repeatedly decompress our file. We start with an `ar archive file` that extracts a `cpio file`. Then we go through multiple compression layers in this order-  
`bzip2` -> `gzip` -> `lzip` -> `lz4` -> `lzma` -> `lzop` -> `lzip` -> `xz`  
After final decompression, found a hex-encoded string-
**7069636f4354467b66316c656e406d335f6d406e3170756c407431306e5f  
6630725f3062326375723137795f33633739633562617d0a**  
Decode it using `xxd -r -p`.
## Flag
**picoCTF{f1len@m3_m@n1pul@t10n_f0r_0b2cur17y_3c79c5ba}**
