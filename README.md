# About this Project
Ultimaco Safeguard was a earlys 2000s Harddrive encryption tool to fully encrypt Harddrives on bootup. This Project shall be a Knowledgebase for everyone who is intrested to gain back access to their data. 
Since SafeGuard is still a ongoing Project from Sophos this project will soley focus on the early adaptations from Ultimaco (Version 1.x to 4.x)

it is important to say that i am no Encryption researcher nor have any deep indepth knowledge on how those encryptions work out, thats why this project exists for others to add to what i have found out so far.

# Software requirements
In order to follow what i have done and reproduce it i reccomend certain softwares:
[VMWARE Workstation Pro](https://www.vmware.com/products/workstation-pro.html)
While i own the full version, the trail should be enough already.

[IMHex](https://github.com/WerWolv/ImHex)
Very good Hex editor

[Disk2VHD](https://learn.microsoft.com/en-us/sysinternals/downloads/disk2vhd)
If you want to make a copy of oyur encrypted Real Harddrive to use in the Virtual machine

# The Documentation
The most important part of understanding how SafeGuard works is a pdf i found on the Internet (**SafeGuard Easy Evaluation Documentation**) describing the internal way how SGE works and is most likley the number 1 Resource for anyone who wants to reverseengineer this:
[Link](https://www.commoncriteriaportal.org/files/epfiles/0176b.pdf)

## About SafeGuards Encryptions algorythms
Following passages where taken out of the  SafeGuard Easy Evaluation Documentation:

**SafeGuard Easy for Windows 2000, Version 1.0** 
6.1.1.1
The TSF shall generate cryptographic keys in accordance with a specified cryptographic key
generation algorithm Random Key Generator (defined in SafeGuard Easy for Windows 2000:
Informal Functional Specification and Correspondence Demonstration, Utimaco, 2001) and
specified cryptographic key sizes 64 bits (56 bits within used by DES) and 128 bits (used by
IDEA) that meet the following: no defined standards.
6.1.1.4
The TSF shall perform symmetric data encryption and decryption of user data on the hard
disk in accordance with a specified cryptographic algorithm IDEA and cryptographic key
sizes 128 bits that meet the following: IDEA standard as published by ASCOM Inc..

This means that if you encounter Safeguard 1.x your computer most likely is Encrypted by DES or IDEA (unknown encryption to me)
Alternativley there was also Blowfish, Stealth, XOR  available.

**Safeguard Easy 4**
While all the old Algorathms where sitll available to choose from. SGE 4.x by default selected AES 256 as default encryption. So its very likley your Harddrive is encrypted with this.

