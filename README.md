# ASUS K53SC OpenCore (based on dubsteptwo's EFI)

## Contents
1. EFI folder
2. Utilities:
  a. macrecovery
  b. GenSMBIOS
  c. USB Tool Box (USB mapping)
## Note
This EFI is based for macOS 10.13

## Prerequisites
- The same exact laptop
- 4 GB+ flash drive
- Windows 10 and up (maybe Windows 8 / 8.1 will work with Python 3, idk)
- Python 3 (>=3.9)
- Some knowlege of what you're doing

## What changed
- Model (from MacBookAir6,1 "Haswell" to 'MacBookPro8,1 "Sandy Bridge") - fixes graphics after 10.13
- USB Mapping (USB 2 for now)

## What doesn't work (still)
- USB 3, webcam (in some apps it works). 

## How to make it work
Download macOS 10.13 with macrecovery using: py macrecovery.py -b Mac-7BA5B2D9E42DDD94 -m 00000000000J80300 download
You need to:
- Format the flash drive (2GB in FAT32 - works the best)
- Put the files in there (EFI and com.apple.reecovery.boot on the root of the drive)
- Set up SMBIOS (just for it to be different)

- Or follow the guide: https://dortania.github.io/OpenCore-Install-Guide
#### Make sure you have enabled UEFI Boot in the BIOS

## How to make it boot from the hard drive

It's kind of easy, you just install the linux distro of your choice, so it creates a boot entry in bios, and shove the files into the efi partition on the drive

## Q&A (kind  of)
Q: WHy graphics didn't work after 10.13?
A: HD3000 isn't supported after 10.13, therefore it  doesn't work
