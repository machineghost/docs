---
title: Using LUKS Disk Encryption with Pop!_OS
description: Learn how to Encrpyt your disk on Install. 
---

Alright, You want to hide your stuff from peeking eyes. The first place to start is disk encryption.

During the installation at the partiton phase, enable disk encryption. LVM is suggested for easy of management.

![image](/images/disk-encryption-luks/enable-encryption.png)

Next, choose an encryption password. Keep this safe!

![image](/images/disk-encryption-luks/enter-password.png)

You may want to over-write your empty space if this is a re-install, so if anybody ever does get a hold of your drive, it won't be possible to take your data.

You're done!
