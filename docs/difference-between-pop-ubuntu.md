---
title: Differences Between Pop!_OS and Ubuntu
description: Learn what makes Pop!_OS different from Ubuntu
---

# Pop!_OS and Ubuntu: What’s the difference?

Pop!_OS is built from Ubuntu repositories, meaning you get the same access to software as Ubuntu. Based on both user feedback and in-house testing, we continue to make changes and updates to the operating system for quality-of-life improvements. The best part is, updates are kept on a rolling release cycle, so you don’t have to wait around 6 months for bug fixes or improvements to your OS.

![General look of desktop](/images/difference-between-pop-ubuntu/pop-desktop-screenshot.png)

## “Isn’t it just a re-skinned Ubuntu?”

This is a common question to come up, and one that makes our engineers cringe. Yes, Pop!_OS has been designed with vibrant colors, a flat theme, and a clean desktop environment, but we created it to do so much more than just look pretty. (Although it does look very pretty.)

To call it a re-skinned Ubuntu brushes over all of the features and quality-of-life improvements that Pop! developers work diligently to create. For an in-depth look at the effort and manpower that goes into updating and maintaining Pop!_OS, take a look at our [Roadmap](https://pop.system76.com/docs/roadmap/) documentation and the [This Week in Pop!](https://pop-planet.info/forums/forums/project-updates.28/) series on [Pop!_Planet](https://pop-planet.info/). Below, you’ll find a general list of improvements that make Pop!_OS stand out.

## First impressions: The Installer 

![Installer Images: Download screen](/images/difference-between-pop-ubuntu/Installer-Screenshot.png)

While Pop!_OS is designed to be [easy to use](https://www.forbes.com/sites/jasonevangelho/2018/11/14/a-linux-noob-reviews-the-pop_os-installer-from-system76/#144a421310d4) for Linux beginners, it’s also developed with the tech-savvy professional in mind. Pop!’s installer sets the tone for our philosophy behind the OS: to provide snappy functionality inside a desktop environment that promotes creative thinking.

The installer offers encryption out of the box and takes care of setting up your user preferences (language, keyboard layout, installation method). On first use, the installer also makes it easy to select your time zone and integrate any online accounts into your desktop.

![Intel/AMD + NVIDIA](/images/difference-between-pop-ubuntu/Intel&AMD-NVIDIA-1904.png)

Pop!_OS comes in two versions: Intel/AMD and NVIDIA. This allows us to include different settings and the proprietary NVIDIA driver for NVIDIA systems, ensuring the best performance and use of CUDA tools one command away. On Oryx Pro systems, you can even switch between Intel and Nvidia graphics using a toggle in the top right corner of your screen.

## Privacy

![Encryption screen](/images/difference-between-pop-ubuntu/Encryption-Screenshot.png)

With encryption enabled by default, and reporting through Ubuntu disabled, Pop!_OS believes that your data should truly be yours. Communications with a third party does not occur by default, and will only occur with user consent.

## Recovery Partition

The recovery partition on this operating system is a full copy of the Pop!_OS installation disk. It can be used exactly the same as if a live disk copy of Pop!_OS was booted from a USB drive. Using the recovery partition, the installed operating system can be repaired or reinstalled. Supported features currently are refresh and clean installs. Refresh installs erase the previously-installed OS while preserving your data stored in the home folder. Fresh installs erase and repartition an entire drive, giving you an install that is identical to what you would get from the factory.

> Refresh Installs are only available on a new install of either Pop!_OS 19.04 or 18.04 (not through upgrading). In the future, it will be possible to initiate a refresh install from within GNOME Settings, if you have a recovery partition. Refresh installs may also be performed when booting a copy of Pop!_OS from a USB drive.

![Recovery](/images/difference-between-pop-ubuntu/recovery.png)

## Improved Desktop Defaults

We want the Pop!_OS desktop to be ready to use as soon as it is installed, without the need for articles recommending "10 Things to Do After Installing Pop!_OS". To that end, we tweak a number of settings and parameters for Linux and the GNOME desktop so that you don't have to. Some of these include the following by default:

- VDPAU / VAAPI support: enabling hardware video decoding in video players
- Vulkan libraries: enabling Vulkan graphics support in 3D applications and games
- Developers have access to `git`, `build-essentials`, and `curl` out of the box
- All non-encrypted swap partitions are created as encrypted swap partitions
- Decreased `vm.swappiness` from 60 to 10, so that swap is used less often
- Enabled modesetting for NVIDIA drivers for improved frame times and responsiveness
- Enabled tap to click by default for touchpads
- LVM and LUKS support
- Complete GVFS support
- Eddy: a graphical tool for installing debian packages
- Popsicle: USB flashing utility

## Default Apps: Slimming down on bloatware 

![Pop Shop](/images/difference-between-pop-ubuntu/pop-shop.png)

Pop!_OS includes a selection of apps intended to be comprehensive, but relatively lightweight. Because Pop!_OS is optimized for your workflow, we avoid providing some larger programs by default that slow down your computer. This is especially true for library applications, such as one for storing your photos, which we opt to replace with image viewers or similar apps that are smaller in size. However, if you’re in need of a photo manager, Steam, or a music streaming app such as Spotify, these applications are still available in the Pop!_Shop for a quick install.

## Third Party Apps

With the desktop as our focus, and as Linux desktop users ourselves, we realize that it's important to include popular applications and tools in our repositories so that can be readily installed on the system without needing third party PPAs. Developers will see that we provide popular tools such as [DBeaver], [Atom], [VS Code], [Slack], and [Mattermost] are readily available in the Shop.

[DBeaver]: https://dbeaver.io/
[Atom]: https://atom.io/
[VS Code]: https://code.visualstudio.com/
[Slack]: https://slack.com/
[Mattermost]: https://mattermost.com/

## Enabling Linux Gaming

System76 hardware is excellent for gaming with, and many of our users are Linux gamers. Vulkan drivers and libraries are installed by default, and the NVIDIA ISO comes with the latest NVIDIA driver installed by default. As new NVIDIA drivers are relased, they are packaged so that you will receive them as regular OS updates. Gamers will also find [Discord], [Lutris], [GameHub], and improved packaging of [Steam] including in our software repositories, and installable through the Shop.

[Discord]: https://discordapp.com/
[Lutris]: https://lutris.net/
[GameHub]: https://tkashkin.tk/projects/gamehub/
[Steam]: https://store.steampowered.com/

## Custom Keyboard Shortcuts

After conducting a study of Ubuntu and GNOME keyboard shortcuts, we decided to make some shortcuts more efficient for common user behaviors. The shortcut for switching workspaces, for example, is <kbd>Super</kbd> + <kbd>Arrow</kbd> <kbd>Up</kbd> or <kbd>Down</kbd>.
[See all keyboard shortcuts](https://pop.system76.com/docs/keyboard-shortcuts/)

## Faster EFI Boots

Most Linux distributions use a bootloader called GRUB, which is essentially a miniature operating system that loads other operating systems. With the advent of EFI firmware and GUID partition tables, it's no longer necessary to boot into a complex bootloader in order to support multi-boot configurations. [systemd-boot] is a simple UEFI boot manager based on the [Boot Loader Specification], which enables the Linux kernel to boot itself with a fraction of the time required by GRUB, and with an simpler configuration format.

> We also developed [kernelstub] as a means to managing the boot loader entries, so that it's easier to add and remove kernel options in the entries that systemd-boot reads at startup.

[systemd-boot]: https://www.freedesktop.org/wiki/Software/systemd/systemd-boot/
[boot loader specification]: https://systemd.io/BOOT_LOADER_SPECIFICATION
[kernelstub]: https://github.com/pop-os/kernelstub/

## Power Daemon

The System76 power daemon provides all the benefits of TLP out of the box, maximizing the battery life of your laptop, supporting multiple power profiles, and switchable graphics modes. An included shell extension provides a power profile picker in the top right menu, which easily toggles between high performance, balanced, and battery saver modes. On systems with supported switchable graphics, this is also where you’ll find the toggle for switching graphics between Intel and NVIDIA. Fan curves on Thelio I/O boards in Thelio desktops are also managed by the power daemon.

![Power Profiles/Graphics toggle](/images/difference-between-pop-ubuntu/system-menu.png)

## Firmware Manager

We created the [firmware manager] as a means of making firmware updates accessible to everyone, whether you are using System76 hardware or otherwise. In Pop!_OS, it is treated as a first class citizen, with integration into GNOME Settings via a new Firmware panel in the Devices category. The Firmware Manager also exists as a standalone application, seamlessly sourcing and applying firmware updates from LVFS and System76.

[firmware manager]: https://github.com/pop-os/firmware-manager

![Firmware Manager](/images/difference-between-pop-ubuntu/firmware-manager.png)

## Popsicle, A Multi-USB Flasher

If you've ever wanted to flash an ISO on multiple USB drives in parallel, we developed [Popsicle] to do exactly that. Select an ISO, select the USB drives to flash to, and watch them flash in parallel.

[popsicle]: https://github.com/pop-os/popsicle

![Popsicle](/images/difference-between-pop-ubuntu/popsicle.png)

## Do Not Disturb

A highly requested feature, Pop!_OS includes the [Do Not Disturb] extension by default. This toggle in the notification panel prevents desktop notifications from displaying when active.

[do not disturb]: https://github.com/pop-os/gnome-shell-extension-do-not-disturb
![Do not Disturb](/images/difference-between-pop-ubuntu/do-not-disturb.png)

## Slim and Dark Theme Variants

Many people prefer the option of toggling between a dark and light theme, and many also prefer to have as minimal spacing around elements in their theme, so we've designed dark and slim variants of the Pop theme, and included toggles in GNOME Settings to make it easier to switch between these variants, without the need to do so through GNOME Tweak Tool.

![Theme switcher](/images/difference-between-pop-ubuntu/theme-variants.png)

## Toggling Mouse Acceleration

Commonly requested of professionals and gamers alike is the ability to specify a flat mouse acceleration profile. This feature, previously hidden away in GNOME Tweak Tool, is front and center in Pop!_OS in the mouse settings panel. With mouse acceleration set to a flat acceleration profile, precision of inputs is improved.

![Mouse acceleration](/images/difference-between-pop-ubuntu/mouse-acceleration.png)

## CUDA SDK / Tensorflow Packaging

Many users System76's customers are using Pop!_OS for scientific workloads, and therefore making the [CUDA SDK] and [Tensorflow] accessible in Pop!_OS is a significant advantage that enables them to get up and running with a development environment quick and painless.

[CUDA SDK]: https://support.system76.com/articles/cuda/
[TensorFlow]: https://support.system76.com/articles/install-tensorflow/

![CUDA/Tensorflow command](/images/difference-between-pop-ubuntu/Tensorflow.png)

## Official Community Resources

Our desktop community is critical to us, as the Linux desktop is our main focus for Pop!_OS, and therefore it is important for our community to be able to discuss the Linux desktop, and Pop!_OS itself. Anyone is free to join the official [Pop!_OS Mattermost instance], where you can communicate with others in Pop!_OS community in realtime. This can be used as a venue for asking quick questions about Pop!_OS.

Issue reports and feature requests are better created in the [appropriate repositories on GitHub], using the [Pop repository] as the general place for all issues which do not fall under a specific project. However, note that any issues regarding System76 hardware are better created as support tickets in your System76 account, as that's where you can reach System76 support.

There is also a community-maintained project, the [Pop! Planet], which many members of our community are using as a platform for discussing ideas, organizing community documentation, and providing support to each other. Pop!_OS progress updates are occasionally posted here, for those who wish to follow what we're doing in Pop!_OS, and it's a great way to discuss bigger topics with our engineers.

We also actively maintain the [Pop!_OS subreddit], for all the Redditors out there.

[Pop!_OS Mattermost instance]: https://chat.pop-os.org/
[appropriate repositories on GitHub]: https://github.com/pop-os/
[Pop repository]: https://github.com/pop-os/pop/
[Pop! Planet]: https://pop-planet.info/forums/
[Pop!_OS subreddit]: https://www.reddit.com/r/pop_os/
