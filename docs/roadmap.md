---
title: Roadmap
description: >
  Focus and features for each release!
---
# Pop!\_OS Roadmap

The 18.04 release is scheduled for April 26th, 2018. This is the second Pop!\_OS release and focuses on encrypted installations, Pop!\_Shop, and a quality experience.

To see how features will be chosen for future releases, visit [pop.system76.com/docs/pop-os-development-approach/](/docs/pop-os-development-approach/)

---

## Installation

Develop a simple and fast installer that introduces users to Pop!\_OS and enables System76 to ship full disk encryption on hardware out of the box.

* ~~Installer backend (https://github.com/pop-os/distinst)~~
* ~~Installer frontend (https://github.com/pop-os/installer)~~
* ~~GNOME Intial Setup (https://github.com/pop-os/gnome-initial-setup)~~

## Pop!\_Shop

* ~~Add Pop!\_OS banner to the home page~~
* ~~Setup a server for curated apps~~
* Determine best-of-class applications and tools for each category
* Button to launch applications after installing
* Propose - buttons to launch and un-install apps on the Updates tab
* ~~Fix issue - applications are listed in reverse order (https://github.com/pop-os/shop/issues/7)~~

## System76 Hardware Recognition

* ~~Installs the System76-Driver on installation~~

## Performance profiles for battery life

* ~~Display in the system menu~~
* ~~Only when a battery is detected~~
* Check GNOME extensions “CPU Power Manager” suggested

## HiDPI Displays

* ~~Package the system76-driver HiDPI daemon separately for Pop!\_OS (https://github.com/pop-os/pop/issues/98)~~
* ~~Create a setting toggle in GNOME Settings Display (https://github.com/pop-os/pop/issues/97)~~
* Correct the projector shortcut issue (https://github.com/pop-os/pop/issues/96)

## GNOME Online Accounts

* Add additional providers to GNOME Initial Setup
* Add CalDav and CardDav providers
* Patch GNOME Calendar and GNOME Contacts for the new providers

---

**Pop!\_OS 17.10**

17.10 was released October 19th, 2017. It is the current release. Struck through work was completed. This is the first Pop!\_OS release and focuses on first use experience, appearance, and default applications.

*Installation*

* ~~Add a feature to Ubiquity to toggle between "minimal" and "complete" Ubiquity. Pop!\_OS will use minimal while other Ubuntu flavors can use the complete.~~ Paired down Ubiquity to a minimal set of screens and packaged seprarately.
* ~~Use GNOME Initial Setup for user configuration~~
* ~~Add nvidia driver to the installation media~~

*Appearance*

* ~~Plymouth work for smooth and beautiful boot to login transitions~~
* ~~Pop!\_Theme refinement~~
* ~~GDM Theme~~

*GNOME Online Accounts*

* Add additional providers to GNOME Initial Setup (incomplete)
* Add CalDav and CardDav providers (incomplete)
* Patch GNOME Calendar and GNOME Contacts for the new providers (incomplete)

*Determine Default applications*

* ~~Choose an email client for the initial release~~
* ~~Determine pre-installed applications~~
