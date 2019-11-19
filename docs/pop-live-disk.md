---
title: Create and Use Bootable Media on Pop!_OS
description: You can run Pop!_OS from a USB drive for hardware testing, recovery, and installation/re-installation.
---

Pop!_OS is remarkably flexible. You can run a full version of Pop!_OS from a USB drive (often known as a thumb drive, flash drive, or USB stick) in what's known as a *live environment*. Using a live environment (live disk) is useful for:

- [Installing Pop!_OS](https://support.system76.com/articles/install-pop/)
- Recovering your existing operating system
- Backing up files when you can't boot
- [Determining if an issue is caused by hardware or software](https://support.system76.com/articles/hardware-failure/)
- [Fixing the boot loader](https://support.system76.com/articles/bootloader/)

A live disk is a handy tool to have around! If you are running Pop!_OS 18.04 then you have a recovery partition which is just like a live disk. You can access this by rebooting your laptop/desktop and tapping the ESC or Space key. There is a menu entry called 'Pop!_OS Recovery', choose that with the arrow keys and then press enter.

Not running Pop!_OS yet? Take a [look here](https://support.system76.com/articles/live-disk/) for instructions on creating a Live USB on other OS's.

## Make Bootable drive

In order to install Pop!_OS, first download the .iso image. This is a disk image with the operating system and installer on it. The download for [Pop!_OS here](http://pop.system76.com). Just click the link and the download should begin!

You'll need a flash drive, of course, and software to write the Pop!_OS .iso image to the drive. There's a variety of applications you can use to write disk images to a flash drive, but for this tutorial you'll use Popsicle.

Popsicle is an open source app for Linux that allows you to "burn images to USB drives safely and easily." It is installed in Pop!_OS 18.04 and up. If you are running Pop!_OS 17.10, you can install it like so in a terminal:

```
sudo apt install popsicle-gtk
```

Once you have installed Popsicle and downloaded the Pop!_OS.iso image, open the Popsicle application.

![Popsicle](/images/pop-live-disk/popsicle.png)

Pick *Choose Image* and navigate to where you downloaded Pop!_OS. Click on it and hit the *open* button:

![Select Pop!_OS iso](/images/pop-live-disk/popsicle-image-selection.png)

Next, select the drive that you want to use. The name of the drive most likely will be the brand name like SanDisk or Kingston.

![Popsicle Flash Drive Selected](/images/pop-live-disk/popsicle-drive-selection.png)

Click the *Flash* button and watch the magic happen!

![Flashing Pop!_OS...](/images/pop-live-disk/popsicle-progress.png)
  
![Flash Complete](/images/pop-live-disk/popsicle-finished.png)

Once the flash is complete (should look like the screenshot above), it's time to boot it up on the machine that you want to install Pop!_OS on!

## Booting From Live Disk

After creating the live disk, insert the USB into your computer, then reboot or power on your system. You'll need to tell the computer to boot from the live disk by holding a key right as you power on:

Laptops                             | Desktops
----------------------------------- | ------------------------------------
Hold <kbd>F7</kbd> or <kbd>F1</kbd> | Hold <kbd>F12</kbd>, <kbd>F8</kbd>, or <kbd>F10</kbd>

If done correctly, you should see a boot device selection menu, like one of the following images.

![Boot Menu](/images/pop-live-disk/boot-menu.jpg)

Use the arrow keys to select the USB drive, then press <kbd>Enter</kbd> to boot the selection.  

Pop!_OS will boot into the installer once you pick your language and keyboard. Select 'Try Demo Mode' in the third slide.

![Live Disk](/images/pop-live-disk/live-desktop.png)

## Using Live Environment

The list provided at the beginning of the article provides links to other articles on using the live environment for hardware testing, restoration/upgrades, and boot repair.

### Repairing Existing Operating System

Since the live environment is a full Pop!_OS installation, it works just like the normal environment. There are tools and methods that allow to `chroot` (change root) into the normal installation and work in the existing operating system to repair a broken package or other problem that is preventing normal booting.

### Backup Files

Perhaps you're reinstalling, or maybe you can't boot but you want to try and recover and back up your files? The live environment will automatically detect and mount most file systems including Linux and Windows. You can access your broken operating system while in a live environment and copy files from the disk to another external disk using the familiar <u>Files</u> utility.
