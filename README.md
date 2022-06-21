# Lenovo ThinkPad T480 OpenCore Hackintosh macOS Moneterey

**Status: Maintained**

**DISCLAIMER:**

Read the entire README and Dortania guides before you start. I am not responsible for any damage.
When you encounter bug or want to improve this repo, consider opening issue or pull request. 
If you find this bootloader configuration useful, consider giving it a star to make it more visible.

## Introduction

<summary><strong>My Hardware</strong></summary>
<br>

| Category  | Component                            | Note                                                                                                               |
| --------- | ------------------------------------ | ------------------------------------------------------------------------------------------------------------------ |
| CPU       | Intel Core i5-8250U                  | 20L50000MC                                                                                                         |
| GPU       | Intel UHD 620                        |                                                                                                                    |
| GPU       | Nvidia GeForce MX 150 4GB            | Disabled                                                                                                           |
| SSD       | Crucial CT500P5SSD8                  | The Stock NVME didn't work in my configuration which                                                               |
| Memory    | 24GB DDR4 2400Mhz                    |                                                                                                                    |
| Battery   | Dual battery                         | macOS only shows one battery                                                                                       |
| Camera    | 720p Camera                          | Not the Windows Hello camera                                                                                       |
| Wifi & BT | Intel Wireless-AC 8265               | Use AirportItlwm for your macOS version and enjoy native Wi-Fi control, or use Heliport app.                       |
| Input     | PS2 Keyboard & Synaptics TrackPad    | [YogaSMC](https://github.com/zhen-zen/YogaSMC) for media keys like microphone switch, etc. PrtSc is mapped as F13. |


<summary><strong>Main software</strong></summary>
<br>

| Component      | Version        |
| -------------- | -------------- |
| macOS Moneterey| 12.4 (21F79)   |
| OpenCore       | v0.8.0         |



## Before installation 

<summary><strong>UEFI settings</strong></summary>
<br>

**Security**

- `Security Chip` **Disabled**
- `Memory Protection -> Execution Prevention` **Enabled**
- `Virtualization -> Intel Virtualization Technology` **Enabled**
- `Virtualization -> Intel VT-d Feature` **Enabled**
- `Anti-Theft -> Computrace -> Current Setting` **Disabled**
- `Secure Boot -> Secure Boot` **Disabled**
- `Intel SGX -> Intel SGX Control` **Disabled**
- `Device Guard` **Disabled**

**Startup**

- `UEFI/Legacy Boot` **UEFI Only**
- `CSM Support` **No**

**Thunderbolt**

- `Thunderbolt BIOS Assist Mode` **Disabled**
- `Wake by Thunderbolt(TM) 3` **Disabled**
- `Security Level` **User Authorization**
- `Support in Pre Boot Environment -> Thunderbolt(TM) device` **Enabled**

## Post-Install

<summary><strong>Generate your own SMBIOS</strong></summary>
<br>

[GenSMBIOS](https://github.com/corpnewt/GenSMBIOS)

- MacBookPro14,1
- MacBookPro15,2
- MacBookPro15,4

## Status

<summary><strong>What's working ✅</strong></summary>

- [x] Battery percentage (Only showing a single percentage)

- [x] Bluetooth - Intel Wireless-AC 8265 (0x0A2B) 

- [x] Boot chime

- [x] GPU UHD 620 hardware acceleration / performance 

- [x] HDMI `Closed and opened lid. With audio.`

- [x] iMessage, FaceTime, App Store, iTunes Store. **Generate your own SMBIOS**

- [x] Intel I219V Ethernet port

- [x] Keyboard `Volume and brightness hotkeys. Another media keys with YogaSMC.`

- [x] Microphone `With keyboard switch using ThinkPad Assistant.`

- [x] Realtek® ALC3287 ("ALC257") Audio

- [x] SD card reader `Fortunately, USB connected.`

- [x] Sidecar wired `Works with 15,2 SMBIOS.`

- [x] Sleep/Wake 

- [x] TouchPad `1-5 fingers swipe works. Emulate force touch using longer and more voluminous touch.`

- [x] TrackPoint  `Works perfectly. Just like on Windows or Linux.`

- [x] USB Ports `USB Map is different for devices with Windows Hello camera.`

- [x] Web camera

- [x] Wifi - Intel Wireless-AC 8265 `Use HeliPort app for Wi-Fi control`

- [x] DRM `Widevine, validated on Firefox 82. WhateverGreen's DRM is broken on Big Sur`


<summary><strong>What's not working ⚠️</strong></summary>

- [ ] Fingerprint reader  `There is finally after many years working driver for Linux (python-validity), don't expect macOS driver any time soon.`

- [ ] PM 981 `Still unstable. Could work for some, not for others.`

- [ ] Sidecar wireless `If you want to use this feature, buy a compatible Broadcom card!`

- [ ] Windows/Linux from OC boot menu `It's best practice to not boot from OC when planning to perform firmware upgrade`


<summary><strong>Untested</strong></summary>

- [ ] Thunderbolt  `No device to test.`
