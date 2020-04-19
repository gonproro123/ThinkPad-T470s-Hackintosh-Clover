# Lenovo Thinkpad T470s Clover
## Introduction

## Thinkpad T470s Hackintosh configuration. This repository contains the following folders:
- `EFI`: put this in your EFI partition in EFI folder, including BOOT, CLOVER & APPLE sub-folders
- `L/E` kexts': kexts that should be installed in `L/E`

## Tested on `Catalina, 10.15.4` with the following hardware:
- Intel i5-7300U
- Intel HD Graphics 620
- 1920x1080 (FHD)
- DDR4 2133 16GB (8Gb x 2)
- Dell Wireless 1560 (BCM94352z)
- Samsung 970evo 250GB NVMe SSD
- Audio : ALC298

## It's a 95% working hackintosh, including:
- Apfs disk partitions: ApfsDriverLoader-64 efi
- Brightness control: AppleBacklightFixup kext
- Audio on speakers: AppleALC kext
- Graphical acceleration (QE/CI): WhatEverGreen kext
- Audio Jack connector
- TrackPoint / Touchpad driver: VoodooPS2.
- Trim enabled

## Bugs
- SD card reader (haven't tested yet)
- Type-C only works as a charging port
- USB next to Type-C port doesn't work
- Speed step seems not perfect (wish you guys help me to improve it <3 )
- P-State ratio * 100 = Frequency in MHz.
- CPU P-States [ 10 31 (35) ] iGPU P-States [ ].
- CPU C3-Cores [ 0 1 3 ].
- CPU C7-Cores [ 1 2 3 ].
- CPU P-States [ 10 12 (25) 31 35 ] iGPU P-States [ ].
- CPU C3-Cores [ 0 1 2 3 ].
- CPU C7-Cores [ 0 1 2 3 ].
- CPU P-States [ 10 12 13 25 (31) 35 ] iGPU P-States [ (18) ].
- CPU P-States [ 10 12 13 25 (31) 35 ] iGPU P-States [ (18) ].
- CPU P-States [ 10 12 13 25 31 (32) 35 ] iGPU P-States [ (18) ].
- CPU P-States [ 10 12 13 25 (30) 31 32 35 ] iGPU P-States [ 18 ].
- CPU P-States [ 10 11 12 13 25 (30) 31 32 35 ] iGPU P-States [ 18 ].
- CPU P-States [ 10 11 12 13 25 (29) 30 31 32 35 ] iGPU P-States [ 18 ].
- CPU P-States [ (8) 10 11 12 13 25 29 30 31 32 35 ] iGPU P-States [ 18 ].
- CPU P-States [ 8 10 11 12 13 (20) 25 29 30 31 32 35 ] iGPU P-States [ 18 ].
- CPU P-States [ 8 10 11 12 13 20 25 29 30 31 32 (33) 35 ] iGPU P-States [ (18) ].
- CPU P-States [ 8 10 11 12 13 20 25 29 30 (31) 32 33 35 ] iGPU P-States [ 18 ].
# Setup
## BIOS Settings
- The BIOS must be properly configured before installing MacOS.

- In `Security menu`, set the following settings:

+ Memory Protection > Execution Prevention: Enabled
+ Virtualization > Intel VT: Disabled (Can be enabled later)
+ Virtualization > Intel VT-d: Disabled (Can be enabled later)
+ Secure Boot > Secure Boot: Disabled
+ Anti-Theft > Current Setting: Disabled
+ Anti-Theft > Computrace > Current Setting: Disabled
+ In the Startup menu, set the following options:

UEFI/Legacy Boot: UEFI Only
CSM Support: Yes
Now you can go through the install.

## What's next?
- To finish the setup, you need to:
+ Install the latest Clover_EFI_bootloader.
+ Copy `EFI folder from USB` flash drive to `local drive EFI partition` (like you did for the USB drive). It will make the local drive bootable (so you can get rid of the USB drive now)
+ Coppy kexts in `L/E_Kexts` into `L/E`

## You're almost done! Reboot and enjoy macOS on your Thinkpad T470s.


# Big thanks to 

- Rehabman.
- Altairko.
- Acidanthera (VoodooPS2)
- Stevezhengshiqi (one-key-cpufriend)


