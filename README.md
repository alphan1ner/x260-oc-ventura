# X260 | oc0.9.2 | macOS 13.4

**System Specifications**

| Spec | Config |
|--|--|
| CPU | i5-6200U |
| iGPU | Intel HD 520 |
| RAM | 16GB DDR4-2133 |
| SSD | Kingston 1TB |
| Wi-Fi | Intel AC8260 |
| OC Ver | 0.9.2 |
| macOS | 13.4 (Ventura) |

This is an EFI config based on OpenCore, tested working on my X260 with macOS Ventura. This is a hardfork of Suhail Sherief's [excellent config](https://github.com/SuhailSherief/ThinkPad-x260-macOS-OpenCore?tab=readme-ov-file), many thanks to him. I created this hardfork as I had made minor tweaks to improve the stability of display outputs, and figured that as I work on this config to suit it to my needs, update kexts, etc, it may become something worthy of sharing. 

I daily drive my X260, and I don't run into any stability issues, but, YMMV. If you would like to hackintosh your X260 and don't know where to start, I reccommend you use [this guide](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/). Please get in touch with any questions or concerns, I am always happy to help! 

Happy Hackintoshing! 

***

**BIOS Settings**

-   `Security -> Security Chip`:  **False**
-   `Memory Protection -> Execution Prevention`:  **True**
-   `Virtualization -> Intel Virtualization Technology`:  **True**
-   `Virtualization -> Vt-Directed IO`:  **False**
-   `Internal Device Access -> Bottom Cover Tamper Detection`: **False**
-   `Anti-Theft -> Computrace -> Current Setting`:  **False**
-   `Secure Boot -> Secure Boot`:  **False**
-   `UEFI/Legacy Boot`:  **UEFI**
-   `CSM Support`:  **False**

**What's Working**

- Display `Hardware-accelerated graphics`
- Trackpad `All 3 hw-buttons and TrackPoint`
- Keyboard Backlight `Same behavior as on Windows/Linux`
- Audio `Integrated only`
- Ethernet 
- Wi-Fi
- iServices `With smBIOS`
- Power Management
- Battery `LPM, Percentage`
- Sleep/Wake/Shutdown
- SD-reader
- HDMI-out `Tested stable at 2560 * 1080 @ 60Hz, thanks to AAPL,GfxYTile patch`
- Dock `DP works at < UHD res, Ethernet works, issues with USB`

**What's Broken**

- DisplayPort `Working, but buggy`
- Bluetooth `Working, but buggy`
