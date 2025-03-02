# Linux Mint XFCE Installation on Macbook Air (2017) 
## Overview 
I installed **Linux Mint XFCE 22.1** on my **MacBook Air**

## System Specifications 
– **Device:** MacBook Air (2017)
– **OS Installed:** Linux Mint 22.1 XFCE
– **Processor:** Intel i5 5350U 2.9GHz
– **RAM:** 8GB
– **Storage:** 256B

## **Installation Summary**
**Created a bootable USB** using Rufus on Windows.
**Booted into Linux Mint Live USB** and started the installer.
**Formated the disk** (completely erased macOS).
**Installed Linux Mint XFCE** successfully.

## **Post-Installation Configurations**
### **System Updates & Security**
```bash
sudo apt update && sudo apt upgrade -y
sudo ufw enable
```
**Updated all packages & enabled firewall**.

## **Checked system info**
```bach
neofetch
lsblk
df -h
```
Verified disk partitions & OS installation.

## **Installed Essential Tools**
```bach
sudo apt install git htop neofetch -y
```

## **Challenges & Fixes**

1. **Wifi Not Working**
– **Issue:** Wifi adapter was not detected after installation.
– **Fix:** Installed Broadcom drivers manually:
```bach
sudo apt install bcmwl-kernel-source -y
```

2. **Boot Mode Verification**
– **Issue:** Needed to confirm if installation was in **UEFI mode**
– **Fix:** Checked with:
```bach
[ -d /sys/firmware/efi ] && echo "UEFI Mode" || echo "Legacy BIOS Mode"
```
Confirmed **UEFI Mode** was enabled.

