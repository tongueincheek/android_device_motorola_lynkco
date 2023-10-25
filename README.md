Device configuration for Motorola Razr 40 / Razr (2023) (lynkco)
=========================================

The Motorola Razr 40 / Razr (2023) (codenamed _"lynkco"_) is a mid-range smartphone from Motorola Mobility announced in June 2023.

## Device specifications

Basic   | Spec Sheet
-------:|:-------------------------
SoC     | Qualcomm SM7450-AB Snapdragon 7 Gen 1 (4 nm)
CPU     | Octa-core (1x2.4 GHz Cortex-A710 & 3x2.36 GHz Cortex-A710 & 4x1.8 GHz Cortex-A510)
GPU     | Adreno 644
Memory  | 8/12 GB RAM (LPDDR5)
Shipped Android Version | 13.0, My UX 3.0 (Global) / MY UI 3.0 (China)
Storage | 128/256/512 GB (UFS 3.1)
Battery | Non-removable Li-Po 4200 mAh (Global) / 5000 mAh (China) battery
Display | 2640 x 1080 pixels, 6.9 inches (~413 ppi density), Foldable LTPO AMOLED, 1B colors, 144Hz, HDR10+, 1400 nits (peak)
Camera  | 64MP (Wide) + 13MP (Ultra-wide) + 32MP (Selfie)

## Device picture
![Motorola Razr 40 (2023)](https://fdn2.gsmarena.com/vv/pics/motorola/motorola-razr-40-2.jpg)

# Status
Current state of features:
- [x] Correct screen/recovery size
- [x] Working touch, display
- [x] Screen goes off and on
- [x] Backup/restore to/from internal/external storage and adb
- [x] Poweroff
- [x] Reboot to system, bootloader, recovery, fastboot, edl
- [x] ADB (including sideload)
- [x] Support EROFS/F2FS/EXT4/exFAT/FAT32/NTFS
- [x] Decrypt /data
- [x] Flashing zip/images
- [x] MTP export
- [x] All important partitions listed in wipe/mount/backup lists
- [x] Input devices via USB-OTG
- [x] USB mass storage export
- [x] Correct date
- [x] Battery level
- [x] Set brightness
- [x] Vibrate and set vibration
- [x] Screenshot
- [x] Advanced features

# Note
In order to `fastboot boot` the compiled image, swap prebuilt/kernel with prebuilt/kernel-real.
This is due to a bootloader quirk where `fastboot flash` uses the kernel from boot partition, while `fastboot boot` expects a bundled kernel in recoveryimage.

# Building
```bash
export ALLOW_MISSING_DEPENDENCIES=true
source build/envsetup.sh
lunch twrp_lynkco-eng
mka recoveryimage -j$(nproc --all)
```

**Copyright (C) 2023 Team Win Recovery Project**
