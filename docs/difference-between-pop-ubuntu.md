---
title: Differences Between Pop!_OS and Ubuntu
description: Learn what makes Pop!_OS different from Ubuntu
---

# What's the difference between Pop!\_OS and Ubuntu?

Pop!\_OS is built from the Ubuntu repositories (meaning you get the same access
to software as Ubuntu), but it's not simply Ubuntu with some changes on top. The
easiest way to see and feel the difference is to give both a try, but this doc
will also give you a fairly expansive run down.

We build Pop!\_OS with a philosophy of sticking to upstream decisions by
default, but deviating when it provides a better experience for our customers
and users. Our decisions around user experience are informed from over a decade
of selling Linux computers and listening to our customers' feedback.

[Learn about our development approach](http://pop.system76.com/docs/pop-os-development-approach/)


## Look & Feel, Session, & Shell

Pop!\_OS uses the Pop! session, a custom GNOME-based session with our default
settings and extensions included.

- Shell theme and GTK stylesheet: A refined, consistent look that is somewhat
  flat while retaining light and shadow
- Fonts: Fira Sans and Roboto Slab to match the Pop! and System76 look
- Suspend button: Always show in the session menu (instead of requiring an extra
  button press)
- Always show workspaces: Don't auto-collapse the workspace switcher in the
  Activities overview
- Right-click to see application details in Pop!\_Shop: Let users quickly learn
  more about and uninstall apps from the dash and app spread
- Plymouth and GDM themes for a consistent look/feel
- Hand-selected set of photographic and illustrative wallpapers for a consistent
  look and feel

Ubuntu 17.10+, on the other hand, includes the Ubuntu session with their own
theme and fonts, plus the "Ubuntu dock" which somewhat imitates the old Unity
launcher.


## Keyboard Shortcuts

We conducted a study of keyboard shortcuts in GNOME and Ubuntu, and derived a
set that more consistently exposes some default behaviors like workspace and
window management.

[See our keyboard shortcuts](http://pop.system76.com/docs/keyboard-shortcuts/)


## Included Apps

Pop!\_OS includes a selection of apps intended to be comprehensive but
relatively lightweight. We avoid "library" apps and instead opt for "viewers";
for example, we don't ship a large photo library management app, but we do
include an image viewer.

[Learn more about our guiding
principles](http://pop.system76.com/docs/default-apps/)

- Eye of GNOME Image Viewer
- Totem Video and Audio Player
- LibreOffice Writer, Calc, and Impress to view, edit, and create docs,
  spreadsheets, and presentations
- Firefox Web Browser
- Geary Email Client
- GNOME Calendar
- Evince Document Viewer
- Pop!\_Shop app store
- Eddy Debian installer

Ubuntu includes a different set of preinstalled apps including GNOME Software,
Rhythmbox, Remmina, Thunderbird, Shotwell, an Amazon affiliate search link, and
several GNOME games.


## Installation and First Use

Pop!\_OS comes in two versions: Intel/AMD and NVIDIA. This allows us to
pre-include different settings and the proprietary NVIDIA driver for NVIDIA
systems, ensuring the best performance and use of CUDA tools right out of the
box.

Every Pop!\_OS installation uses an OEM-like install process, leaning on GNOME
Initial Setup for both first user and additional user setup. This means there
are fewer paths to an installed system which reduces the load for testing as
well as the opportunities for bugs.

GNOME Online Accounts and GNOME Initial Setup in Pop!\_OS have also been
modified to add additional account providers including CalDav and CardDav for
better calendar and contacts integration in the OS.

Ubuntu comes with one version and requires the manual installation of NVIDIA
drivers and tools after the fact for NVIDIA systems. Ubuntu also uses the
Ubiquity installer for first user setup instead of GNOME Initial Setup.
