# ASUS K53SC OpenCore (based on dubsteptwo's EFI)

## What changed
- Model (from MacBookAir6,1 "Haswell" to 'MacBookPro8,1 "Sandy Bridge") - fixes graphics after 10.13
- USB Mapping (USB 2 for now)

## What doesn't work (still)

- USB 3, webcam (in some apps it works). 

## How to use

follow along this guide https://dortania.github.io/OpenCore-Install-Guide/, you can skip the bits where you actually do stuff, but you do need to
- format the flash drive (2GB in FAT32 - works the best)
- put the stuff in there
- set up SMBIOS (just for it to be different)
#### Make sure you have enabled UEFI Boot in the BIOS

## How to make it boot from the hard drive

It's kind of easy, you just install the linux distro of your choice, so it creates a boot entry in bios, and shove the files into the efi partition on the drive
