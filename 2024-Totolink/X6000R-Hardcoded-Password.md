# Title
- **Exploit Title:** X6000R_Hardcoded_Password
- **Date:** 2024/02/02
- **Exploit Author:** WoodMan
- **Vendor Homepage:** https://www.totolink.net
- **Software Link:** https://www.totolink.net/home/menu/detail/menu_listtpl/download/id/247/ids/36.html
- **Version:** V9.4.0cu.852_B20230719
- **Tested on:** 2024/02/02
- **Payload:** `john --format=md5crypt --wordlist=/usr/share/wordlists/rockyou.txt etc/shadow`
- **CVE:** Reported, waiting for CVE Number

## Description
TOTOLINK X6000R V9.4.0cu.852_B20230719 was discovered to contain a hardcoded password for root stored in /etc/shadow.

## Proof of Concept
1. Download firmware version V9.4.0cu.852_B20230719.
2. Use unrar to extract the files.
3. Use 7z to unpack the .web file.
4. Employ Payload to perform a brute force attack on /etc/shadow.
