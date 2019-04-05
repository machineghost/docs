---
title: Roadmap
description: >
  Focus and features for each release!
---
# Pop!_OS Roadmap

This road map details features which are currently-planned to be implemented in Pop!_OS, as well
as major features which were added to Pop!_OS during previous release cycles. Only features
specific to Pop!_OS will be listed here. To see how features are chosen, see the
[Pop!_OS Development Approach page](/docs/pop-os-development-approach/).

However, note that feature development in Pop!_OS is not exclusive to any particular point release,
as we follow a rolling-release strategy for updates to projects which we maintain. This means that
features are added to Pop!_OS as soon as they are finished, instead of being withheld to the next
point release. When features are completed, they are added to the latest "stable" and
"long term stable (LTS)" point releases, whenever possible.

---

## Currently-Planned Features

These are features which we would either like to, or are already in the process of, implementing.
As these are completed, they will be listed underneath a release cycle, indicating which cycle
the feature was implemented during. When a feature is listed as being implemented during the 19.04
release cycle, this means that it was completed before 19.04 was released, and thus was available
on release for 19.04.

### GNOME Online Accounts

* Add additional providers to GNOME Initial Setup
* Add CalDav and CardDav providers
* Patch GNOME Calendar and GNOME Contacts for the new providers

### Installer

* Alongside OS installation option
* Resizing LUKS and LVM partitions
* Create Rust bindings for blkid, devmapper, and cryptsetup
* Create Rust crates for disk-probing and management
* Separate disk management from the installer
* Providing distinst as a daemon for the installer
* Enabling Wayland support for the installer
* Support for exotic LUKS and LVM combinations
* LVM snapshotting support
* Support for special features in ZFS
* Support for ZFS and its special features

### System76 Power

* Configurable power profiles
* Custom commands for power profile switches
* Additional power-saving features enabled by default
* Power profiles for non-Intel processors
* Power profiles for AMD and NVIDIA graphics

### Popsicle

* Support for creating bootable Windows 10 drives
* Imaging from an existing drive to many other drives
* Performing I/O with `std::future::Future` when it is stable
* Internationalization support, with [Project Fluent](https://projectfluent.org/).

### Pop Upgrade

* Reduce the bandwidth required to update the recovery partition
* Support fetching apt URIs without help from `apt-get`
* Improved detection of packages and possible package-conflicts

### Packaging

Rethinking the `debrep` approach may be ideal for the future. A redesigned `debrep` with support
for the following features would be useful:

* Mirroring apt repositories when defining their URL in a TOML spec.
* A database for tracking which packages have been built, and which packages are to be added.
* A packaging CI for watching changes to git repositories, automatically building
  them as new commits are made, and uploading them to the repository.
* Possibly a simple web UI for internally managing a repository, similar to Launchpad.

---

## Pop!_OS 19.04 (current development)

Pop!_OS 19.04 is scheduled to release on April 18th, 2019.

### Installation

* A handful of bugs were reported and fixed during this cycle.
* A few additional system checks were added to prevent incompatible installation setups.
* EFI partitions now require at least 500 MiB, to decrease the likelihood of issue reports
  consisting of no-space-left errors.

### Packaging

The following packages were added / updated during this release.

* GameHub
* Geary 3.32 backported to bionic and cosmic
* GNOME Authenticator
* GNOME Podcasts
* Lollypop
* Lutris
* PulseEffects
* Steam 1.0.0.59

### Popsicle

* The GTK UI was rewritten using a better architecture for UI app development.
  * The code is now easier to maintain, due to being less complex, and having less of it.
  * UI is now more responsive than before, so the chance of the UI hanging is now impossible.
* A bug was fixed that would cause systems with card readers to indefinitely hang.

#### Refresh OS Installations

Two features have been developed during this cycle: "Refresh" and "Alongside OS" installation
options. The refresh feature was the first to be complete, providing the ability to retain
user accounts and files while reinstalling the OS. The alongside OS option will follow shortly
after.

### System76 Power

* Fan controls have been improved in this release.
* The daemon now actively knows which state is currently set.
* Signals to listening clients are now sent when the power profile is changed.

### Upgrade Daemon

Due to the many issues experienced with Ubuntu's `do-release-upgade` script, a new project was
started during this cycle to improve the reliability of release upgrades. This daemon is
responsible for perform system repairs and preparing the system for a release upgrade.

* Adds the ability to upgrade the recovery partition.
* Adds the ability to perform a release upgrade offline with systemd and the recovery partition.
* Offline installs with systemd will boot into a minimal environment to perform the upgrade,
  and reboot when finished.
* As with `system76-power`, it provides a CLI frontend in the same binary that the daemon
  launches from.
* Some limited forms of repairing possible system errors that would prevent a release upgrade.
* Provides a daemon that can be used to check for release upgrades

---

## Pop!_OS 18.10

Released on October 20th, 2018, the focus of development was furthered improvements to the
reliablity and feature set provided by our distribution installer; the addition of many third
party applications, including Tensorflow; and the inclusion

### Installation

* All bugs reported against the new installer were fixed during this cycle.
  * Many system checks were added to prevent incompatible installation setups.
  * A new crate for managing keyboard and language locales was developed.
  * Setting the correct keyboard layout for the cryptsetup screen was fixed.
* Various portions of distinst were separated into multiple crates.
* Improved support for detecting required packages based on installation configuration, and
  removal of packages which are not necessary for that configuration.

### Packaging

* `debrep` was created to experiment with building our own apt repositories from a TOML spec.
* A third party repository was created from `debrep` for storing packages fetched from third
  party resources, as well as NVIDIA and Tensorflow packaging.
* Many popular applications were added to the repositories, with more to come in the future.

### Pop!_Shop

* Various actions throughout the UI would cause the application to hang. Patches were submitted
  upstream to elementary to prevent the UI from freezing.
* A patch for a screenshot cache and parallel fetching of screenshots was also submitted.

### System76 Power

* Fan controls were added, with support for Thelio's I/O boards.
* The CLI now handles arguments via the `clap` crate, to provide a quality user-friendly interface.
* A new `--experimental` flag was added for the daemon to launch with additional Powertop and
  TLP-recommended power-saving options.

---

## Pop!_OS 18.04

Released on April 26th, 2018, the focus of development was a new installer that supports encrypted
installations, integration of the Pop!\_Shop, the addition of a multiple USB file flasher utility
(Popsicle), and overall improvements to the desktop experience.

### HiDPI Displays

* Package the system76-driver HiDPI daemon separately for Pop!_OS (https://github.com/pop-os/pop/issues/98)
* Create a setting toggle in GNOME Settings Display (https://github.com/pop-os/pop/issues/97)
* Correct the projector shortcut issue (https://github.com/pop-os/pop/issues/96)

### Installation

Develop a simple and fast installer that introduces users to Pop!_OS and enables System76 to ship full disk encryption on hardware out of the box.

* Installer backend (https://github.com/pop-os/distinst)
* Installer frontend (https://github.com/pop-os/installer)
* GNOME Intial Setup (https://github.com/pop-os/gnome-initial-setup)
* On detection of system76 hardware, the `system76-driver` package is installed.
* With the NVIDIA ISO on non-NVIDIA hardware, the nvidia drivers are removed.

### Pop!\_Shop

* Add Pop!_OS banner to the home page
* Setup a server for curated apps
* Determine best-of-class applications and tools for each category
* Button to launch applications after installing
* Fix issue - applications are listed in reverse order (https://github.com/pop-os/shop/issues/7)

### System76 Power

* A new daemon was developed that provides and controls power profiles.
* Added a shell extension to provide the UI options in the desktop to control these profiles.
  * These controls are only displayed if a battery is detected on the system.

---

## Pop!_OS 17.10

17.10 was released October 19th, 2017. It is the current release. Struck through work was completed. This is the first Pop!_OS release and focuses on first use experience, appearance, and default applications.

### Appearance

* Plymouth work for smooth and beautiful boot to login transitions
* Pop!\_Theme refinement
* GDM Theme

### Determine Default applications

* Choose an email client for the initial release
* Determine pre-installed applications

### Installation

* Add a feature to Ubiquity to toggle between "minimal" and "complete" Ubiquity. Pop!_OS will use minimal while other Ubuntu flavors can use the complete. Paired down Ubiquity to a minimal set of screens and packaged seprarately.
* Use GNOME Initial Setup for user configuration
* Add nvidia driver to the installation media
