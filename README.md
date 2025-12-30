# ASUS K53SC Opencore
(based on dubsteptwo's EFI)

## Contents
1. EFI folder
2. Utilities:
   1. macrecovery
   2. GenSMBIOS
   3. USBToolBox (USB mapping)

## Note
This EFI is based for macOS 10.13

## Prerequisites
- The same exact laptop
- 2 GB+ flash drive (fast one is recommended)
- Windows 10 and up (maybe Windows 8 / 8.1 will work with Python 3, idk)
- Python 3 (>=3.9)
- Some knowlege of what you're doing

## What changed
- Model (from MacBookAir6,1 "Haswell" to 'MacBookPro8,1 "Sandy Bridge") - fixes graphics after 10.13
- USB Mapping (USB 2 only)
- Added NullCPUPowerManagement.kext, won't boot without it

## What doesn't work (still)
- USB 3, webcam

## How to make it work
Download macOS 10.13 with macrecovery using either: 
   1. py macrecovery.py -b Mac-7BA5B2D9E42DDD94 -m 00000000000J80300 download
   2. py macrecovery.py -b Mac-BE088AF8C5EB4FA2 -m 00000000000J80300 download
- You need to:
- Format the flash drive (2GB in FAT32 - works the best)
- Put the files in there (EFI and com.apple.reecovery.boot on the root of the drive)
- Set up SMBIOS (just for it to be different)

Or follow the guide: https://dortania.github.io/OpenCore-Install-Guide

#### Recommended to remap USB via USBToolBox:
1. Go to "C. Change Settings" -> enable both Native Classes and Legacy Native Classes (N and L), then B to get back
2. Go to "D. Discovr Ports" -> connect any USB device to every USB port, then B to get back
3. Go to "S. Select Ports And Build Kext" -> K. Build Kext -> enter "MacBookPro8,1"
4. Copy the USBMapLegacy.kext folder to "Kexts" foldr in OC

#### Make sure you have enabled UEFI Boot in the BIOS

## How to make it boot from the hard drive

It's kind of easy, you just install the linux distro of your choice, so it creates a boot entry in bios, and shove the files into the efi partition on the drive
