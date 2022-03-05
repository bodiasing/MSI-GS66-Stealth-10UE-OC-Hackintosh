# MSI-GS66-Stealth-10UE-OC-Hackintosh
# I have been creating this EFI for a long time, and I wanted to share who has the same model of MSI as I have
| Specifications | Details |
|:-: |:-: |
| Processor | i7-10750H 6 Core  |
| RAM | 16GB DDR4 |
| SSD | NWME PM981a 1T(disabled with SSDT)+Samsung 970 Evo Plus 2TB |
| iGPU| Intel UHD Graphics 630 |
| DGPU | Nvidia GeForce RTX 3060 (disabled with -wegnoegpu and SSDT-PTSWAK, SSDT-NoHybGfx) |
| Monitor | 15.6" Full HD 240Hz (LQ156M1JW03) |
| Sound | Dynaudio Speakers 2W |
| Network Card | Killer Gb LAN  (Intel AX210NGW) |
| OS Version | Big Sur 11.6.4 |

# Current Functionality

| Function | Performance |
|:-: |:-: |
| USB Patching | Excellent |
| Sleep* | Excellent |
| Disable dGPU | Excellent |
| Enable iGPU | Excellent |
| Audio | Excellent (VoodooHDA 299) (See how to install on bigsur) | 
| WiFi** | Very Good with AirportItlwm.kext|
| Ethernet | Excellent|
| Bluetooth | Good |
| Thunderbolt | Very Good|
| CPU Optimisation | Excellent |
| Battery | Good |
| Brightness & Sound Keys | Excellent |
| General stability | Excellent |

#
#### To enter the Advanced BIOS
Not necessarily, but I updated the BIOS to the latest version of E16V3IMS.111
While in the BIOS, press F2, Left ALT, Right SHIFT, Right CTRL
Now you can verify that DVMT Pre-Allocated is set to 64MB and DVMT Total Gfx Mem is set to Max
Also, and most important, set CFG Lock to Disabled, to enable native PM (also you would probably get a KP without it, if using current version of the EFI)

#### IMPORTANT

Please generate a new SMBIOS (MacBookPro16,1 or MacBookPro16,4) as I deleted my serials. 
Use https://github.com/corpnewt/GenSMBIOS
