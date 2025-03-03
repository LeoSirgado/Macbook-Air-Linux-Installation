# Linux Mint XFCE Installation on Macbook Air (2017) 
## Overview 
This project involved installing **Linux Mint XFCE 22.1** on my **MacBook Air** to establish a dedicated environment for hands-on learning and the development of Linux system administration and IT support skills. 

## System Specifications 
– **Device:** MacBook Air (2017)
– **OS Installed:** Linux Mint 22.1 XFCE
– **Processor:** Intel i5 5350U 2.9GHz
– **RAM:** 8GB
– **Storage:** 256GB

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
Updated all packages & enabled firewall.

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

## **Screenschots**
### 1. **System Information**
#### **OS & Hardware Details**
https://github.com/LeoSirgado/Macbook-Air-Linux-Installation/blob/main/neofetch.png
#### **Storage & Partition Layout**
https://github.com/LeoSirgado/Macbook-Air-Linux-Installation/blob/main/lsblk.png
https://github.com/LeoSirgado/Macbook-Air-Linux-Installation/blob/main/df-h.png
#### **Boot Mode (UEFI/Legacy)**
https://github.com/LeoSirgado/Macbook-Air-Linux-Installation/blob/main/UEFI%20Mode.png
### 2. **Network & Wireless Configuration**
#### **Network Adapter Information**
https://github.com/LeoSirgado/Macbook-Air-Linux-Installation/blob/main/grep%20Broadcom.png
#### **IP Configuration**
https://github.com/LeoSirgado/Macbook-Air-Linux-Installation/blob/main/ifconfig.png
#### **Wi-fi Driver Logs**
https://github.com/LeoSirgado/Macbook-Air-Linux-Installation/blob/main/grep%20wl.png
### 3. **Security & Firewall**
#### **Firewall Status**
https://github.com/LeoSirgado/Macbook-Air-Linux-Installation/blob/main/ufw-status.png
### 4. **Desktop Environment**
#### **Linux Mint Desktop**
https://github.com/LeoSirgado/Macbook-Air-Linux-Installation/blob/main/mint%20desktop.png

## **What i Learned**
–**Linux System Management**: I learned how to manage a Linux system, including updating packages and configuring the firewall using UFW.
–**System Information Tools**: I became familiar with tools like `neofetch`, `lsblk`, and `df -h` to view system information and disk usage.
–**Networking Basics**: I gained hands-on experience with commands like `lspci` and `ifconfig` for inspecting network and hardware configurations.
–**Troubleshooting**: I practiced troubleshooting common issues by reviewing logs with `dmesg` and checking system status using `ufw`.
–**Dcoumentation Skills**: I improved my ability to documnet technical processes clearly, wich is crucial for IT support roles.

## **Conclusion**
This project provided my first hands-on experience with Linux system administration and IT support. It helped me learn basic tasks such as configuring the firewall, gathering system information, troubleshooting and laid a strong foundation for my future learning and growth in IT support roles. 
