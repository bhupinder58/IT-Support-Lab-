# 💾 Windows 10/11 Installation Guide

## 🎯 Goal

Perform a clean Windows installation on physical PC or VM for lab testing.

## 🔧 Tools Required

- 8GB+ USB drive
- [Rufus](https://rufus.ie) (for making bootable USB)
- Windows ISO from [Microsoft](https://www.microsoft.com/software-download/)

## 📝 Steps

1. **Download Windows ISO**
   - Visit Microsoft's website
   - Download the Media Creation Tool or ISO

2. **Create Bootable USB**
   - Open Rufus
   - Select USB device
   - Select ISO
   - Use MBR (for BIOS) or GPT (for UEFI) depending on system

3. **Install Windows**
   - Boot from USB (change boot order in BIOS)
   - Select “Custom Install”
   - Delete all old partitions
   - Let it create new ones and install

4. **First Boot Setup**
   - Skip Microsoft account (use offline)
   - Set admin password
   - Name computer
   - Wait for desktop to load

5. **Drivers**
   - Use `Device Manager` to check missing drivers
   - Download chipset, LAN/Wi-Fi, display drivers if needed

