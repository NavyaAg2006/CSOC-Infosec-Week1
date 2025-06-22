# Task25 - CrypTOYminers Sing Volala-lala-latility
### 1. What is the exposed password that we find from the bash history output?
Use the command-
```bash
vol.py -f linux.mem --profile="LinuxUbuntu_5_4_0-163-generic_profilex64" linux_bash
```
In the following line in the output we see the password-  
_10205 bash  2023-10-02 18:19:58 UTC+0000   mysql -u root -p'NEhX4VSrN7sV'_  
- **Ans:** `NEhX4VSrN7sV`
### 2. What is the PID of the miner process that we find?
Use the command-
```bash
vol.py -f linux.mem --profile="LinuxUbuntu_5_4_0-163-generic_profilex64" linux_pslist
```
In the output we can see-  
_0xffff9ce9b1e4c680 miner  10280   1  1000   1000   0x0000000074fa2000 2023-10-02 18:22:37 UTC+0000_  
- **Ans:** `10280`
### 3. What is the MD5 hash of the miner process?
In the **extracted** directory, use the command
```bash
md5sum miner.10280.0x400000
```
- **Ans:** `153a5c8efe4aa3be240e5dc645480dee`
### 4. What is the MD5 hash of the mysqlserver process?
In the **extracted** directory, use the command
```bash
md5sum mysqlserver.10291.0x400000
```
- **Ans:** `c586e774bb2aa17819d7faae18dad7d1`
### 5. Use the command [ strings extracted/miner.<PID from question 2>.0x400000 | grep http:// ]. What is the suspicious URL? (Fully defang the URL using CyberChef)
We find the URL **http://mcgreedysecretc2.thminsufficient**.  
Go to [CyberChef](https://gchq.github.io/CyberChef/) and use **defang URL** on the URL found.
- **Ans:** `hxxp[://]mcgreedysecretc2[.]thminsufficient`
### 6. After reading the elfie file, what location is the mysqlserver process dropped in on the file system?
In the **extracted** directory use the command
```bash
cat elfie
```
In the output we see the path-
- **Ans:** `/var/tmp/.system-python3.8-Updates/mysqlserver`
