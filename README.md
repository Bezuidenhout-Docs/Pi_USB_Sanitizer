![CIRCLean Version](https://img.shields.io/badge/CIRCLean-v3.0.0-blue)

<!-- BADGES START -->
<p align="center">
  <img src="https://img.shields.io/badge/Raspberry%20Pi-3B%2B-A22846?logo=raspberry-pi&logoColor=white" alt="Raspberry Pi">
  <img src="https://img.shields.io/badge/CIRCLean-v3.0.0-blue" alt="CIRCLean">
  <img src="https://img.shields.io/badge/License-GPL%203.0-green" alt="License">
  <img src="https://img.shields.io/badge/Status-Working-brightgreen" alt="Status">
  <br>
  <img src="https://img.shields.io/badge/Platform-Linux-orange" alt="Platform">
  <img src="https://img.shields.io/badge/Security-Grade%20B-yellow" alt="Security">
  <img src="https://img.shields.io/badge/Flashing-Rufus-orange?logo=windows" alt="Flashing Tool">
  <img src="https://img.shields.io/badge/Made%20with-Raspberry%20Pi-red" alt="Made with">
  <br>
  <img src="https://img.shields.io/badge/Open%20Source-❤️-purple" alt="Open Source">
  <img src="https://img.shields.io/badge/PRs-Welcome-brightgreen" alt="PRs Welcome">
  <img src="https://img.shields.io/badge/Version-1.0.0-informational" alt="Version">
  <img src="https://img.shields.io/badge/Last%20Updated-2026-blue" alt="Last Updated">
  <img src="https://img.shields.io/badge/Flashed%20with-Rufus-success?logo=windows" alt="Flashed with">
</p>
<!-- BADGES END -->

Overview
🛡️ Turn your Raspberry Pi into a USB bodyguard

This project turns a Raspberry Pi 3 B into a dedicated USB sanitizer that safely processes files from untrusted USB drives. Built using CIRCLean (an open-source tool from CIRCL, Luxembourg's national Computer Emergency Response Team), the device acts as a secure intermediary between suspicious drives and your main computer.

How It Works






When an untrusted USB drive is inserted into the top port and a clean drive into a bottom port, the Raspberry Pi automatically:

Action	Description
🔄 Converts	Word docs, PDFs, Excel sheets → safer HTML format
⚠️ Flags	Renames .exe files with DANGEROUS_ prefix
📦 Unpacks	Sanitizes archive files (ZIP, etc.)
🎵 Plays	Music while processing (audio feedback)
🔌 Shuts down	Automatically when finished
Hardware Requirements
Item	Status
💾 Untrusted USB (source)	Required
💾 Trusted USB (destination - FAT32)	Required
🎧 Headphones/speaker	Optional
Software Required
CIRCLean disk image - Download from circl.lu

Rufus - Windows flashing tool (rufus.ie)

Setup Instructions (with Rufus)
bash
# 1. Download CIRCLean image from official website
#    https://www.circl.lu/projects/CIRCLean/

# 2. Open Rufus on your Windows computer

# 3. Insert your microSD card into your computer

# 4. In Rufus:
#    - Select your microSD card under "Device"
#    - Click "SELECT" and choose the CIRCLean image
#    - Leave all other settings as default

# 5. Click "START" and confirm any warnings

# 6. Wait for Rufus to complete flashing

# 7. Safely eject the microSD card

# 8. Insert SD card into Raspberry Pi
Usage
text
┌─────────────────────────────────────────────────┐
│  STEP 1: Power OFF the Raspberry Pi             │
├─────────────────────────────────────────────────┤
│  STEP 2: Insert 💀 UNTRUSTED USB → TOP port     │
├─────────────────────────────────────────────────┤
│  STEP 3: Insert ✅ CLEAN USB → BOTTOM port      │
├─────────────────────────────────────────────────┤
│  STEP 4: Power ON the Raspberry Pi              │
├─────────────────────────────────────────────────┤
│  STEP 5: Wait for 🎵 to stop                    │
├─────────────────────────────────────────────────┤
│  STEP 6: Remove drives (auto-shutdown)          │
├─────────────────────────────────────────────────┤
│  STEP 7: Access sanitized files on clean USB    │
└─────────────────────────────────────────────────┘
Security Notes
Risk Level	Description
⚠️ Medium	Pi itself could be targeted by sophisticated malware
✅ Best Practice	Re-flash SD card (using Rufus) after each use
💾 Pro Tip	Keep a clean master image saved on your computer
🚫 Limitation	Does NOT protect against BadUSB hardware attacks
Status
✅ Device working

🔄 File conversion functional

🎵 Audio feedback working

🔌 Auto-shutdown working

📀 Flashed successfully with Rufus

Limitations
Destination drive must be FAT32 ❌ (exFAT not supported)

Slow processing on Pi 3 B 🐢

Not immune to all USB attacks

Credits
CIRCL - circl.lu for developing CIRCLean

Raspberry Pi Foundation - raspberrypi.org

Rufus - rufus.ie for the excellent flashing tool

