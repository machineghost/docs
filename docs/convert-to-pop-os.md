---
title: Convert Ubuntu to Pop\!\_OS
---
An installation of Ubuntu (17.04+) can be converted to Pop\!\_OS by running the following commands.

```
sudo add-apt-repository ppa:system76/pop
sudo apt update
sudo apt install pop-desktop
```

Following that you may have to reset your gsettings in order to make everything work correctly, but **do so only if you experience issues**.

```
gsettings list-schemas | xargs -n 1 gsettings reset-recursively
```
