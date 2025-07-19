# Macbook-Notes

## Install
Option+Power

## Disks
```
Device             Start       End   Sectors   Size Type
/dev/nvme0n1p1       512     77311     76800   300M EFI System
/dev/nvme0n1p2     77312 117649540 117572229 448.5G Linux filesystem
/dev/nvme0n1p3 117649541 122126129   4476589  17.1G Linux swap
```

## Wireless
```
$ lspci | grep -i network
03:00.0 Network controller: Broadcom Inc. and subsidiaries BCM43602 802.11ac Wireless LAN SoC (rev 02)
```

BCM43602 needs the brcmfmac.feature_disable=0x82000 kernel parameter as tested with PCI Device ID 14e4:43ba (see BBS#298025).
```
cat /boot/loader/entries/2023-02-24_00-11-00_linux.conf 
# Created by: archinstall
# Created on: 2023-02-24_00-11-00
title Arch Linux (linux)
linux /vmlinuz-linux
initrd /intel-ucode.img
initrd /initramfs-linux.img
options root=PARTUUID=7473a00c-41ec-4579-b9d3-40762bab0c66 zswap.enabled=0 rw intel_pstate=no_hwp rootfstype=ext4 brcmfmac.feature_disable=0x82000

```

[Source](https://wiki.archlinux.org/title/Broadcom_wireless#BCM43602_802.11ac_Wireless_LAN_SoC).
## Links
* https://github.com/Dunedan/mbp-2016-linux
* https://gist.github.com/roadrunner2/1289542a748d9a104e7baec6a92f9cd7

## Info Center
* Operating System: Kubuntu 23.04
* KDE Plasma Version: 5.26.4
* KDE Frameworks Version: 5.101.0
* Qt Version: 5.15.6
* Kernel Version: 5.19.0-21-generic (64-bit)
* Graphics Platform: Wayland
* Processors: 8 × Intel® Core™ i7-7700HQ CPU @ 2.80GHz
* Memory: 15.5 GiB of RAM
* Graphics Processor: AMD Radeon RX Graphics
* Manufacturer: Apple Inc.
* Product Name: MacBookPro14,3
* System Version: 1.0

## MacOS Screenshots
* Cmd+Shift+4 — Select an area, saves to desktop
* Cmd+Ctrl+Shift+4 — Select an area, copies to clipboard — my favorite!
