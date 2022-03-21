# MSI-GS66-Stealth-10UE-OC-Hackintosh

# UPDATE "EFI UPDATE"
I replaced voodoohda.kext with applealc.kext and use verbstub.kext.

But you need to install ComboJackfix (included in "EFI UPDATE").

Your folder path must be, my folder path is specified in the terminal.

Installation in the terminal:

    cd ~/Downloads/ComboJackfix    
    sh install.sh      

# I have been creating this EFI for a long time, and I wanted to share who has the same model of MSI.

| Specifications | Details |
|:-: |:-: |
| Processor | i7-10750H 6 Core  |
| RAM | 16GB DDR4 |
| SSD | NVME PM981a 1TB (disabled with SSDT) + Samsung 970 Evo Plus 2TB |
| iGPU| Intel UHD Graphics 630 |
| DGPU | Nvidia GeForce RTX 3060 (disabled with -wegnoegpu and SSDT-PTSWAK, SSDT-NoHybGfx) |
| Monitor | 15.6" Full HD 240Hz (LQ156M1JW03) |
| Sound | (ALC298) Dynaudio Speakers 2W |
| Network Card | Killer E3100X Gb LAN  (Intel AX210NGW) |
| OS Version | Big Sur 11.6.4 (20G417) OC 0.7.9 | 

# Current Functionality

| Function | Performance |
|:-: |:-: |
| USB Patching | Excellent |
| Sleep | Excellent |
| Disable dGPU | Excellent |
| Enable iGPU | Excellent |
| 240hz Support | Excellent |
| Audio (ALC298) | Excellent (update Applealc.kext, layout id - 72 and ComboJackfix) | 
| WiFi | Very Good |
| Ethernet | Excellent|
| Bluetooth | Good |
| Thunderbolt 3 (JHL7540) | Not tested|
| CPU Optimization | Excellent |
| Battery | Good |
| Brightness & Sound Keys | Excellent |
| Trackpad & Gestures| Excellent |
| General stability | Excellent |

#
#### To enter the Advanced BIOS
Not necessarily, but I updated the BIOS on the latest version of E16V3IMS.111, and undervolted -105 mv.
While in the BIOS, press F2, Left ALT, Right SHIFT, Right CTRL
Now you can verify that DVMT Pre-Allocated is set to 64MB and DVMT Total Gfx Mem is set to Max. Disabled Fast boot and Secure boot.
Also, and most important, set CFG Lock to Disabled, to enable native PM (also you would probably get a KP without it, if using current version of the EFI)

My bios settings:

DVMT Pre-Allocated is set to 64MB

DVMT Total Gfx Mem is set to Max Also

CFG Lock to Disabled

Enable native ASPM

Secure boot - disable

Fastboot - disable

Boot mode - uefi

Undervolted - -105 mv

Turbo boost lock - x40 all six cores

Memory timing:

18

19

42

19

480

Nmode - 1

Command rate support cmds3

#### IMPORTANT

Please generate a new SMBIOS (MacBookPro16,1 or MacBookPro16,4) as I deleted my serials. 
Use https://github.com/corpnewt/GenSMBIOS
