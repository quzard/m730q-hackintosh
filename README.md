# OpenCore EFI for Lenovo M730Q (macOS 12.1)
## Just for backup

## Specification
| **Component** | **Model** |
| ------------- | --------- |
| CPU | Intel i5-10500T |
| RAM | 2 * 8GB DDR4-2133 |
| Audio Chipset | ALC233 |
| GPU | Intel® UHD Graphics 630 (DP, HDMI, VGA) |
| OS Disk (NVMe) | LITEON T10 NVMe 256G |
| WIFI | Intel 7265 |
| Ethernet | Intel I219-V |

**macOS version**: 12.1
**OpenCore version**: 0.7.6

## How to use

1. Make your USB installer with [**this guide**](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/)
2. Clone the repository and paste "BOOT" and "OC" directories into your's pendrive "EFI" folder
3. Download [**GenSMBIOS**](https://github.com/corpnewt/GenSMBIOS) to generate unique SMBIOS information. Run it and select **Generate SMBIOS**, as the model select **iMac20,1**.
4. Open config.plist with [**ProperTree**](https://github.com/corpnewt/ProperTree) and go to PlatformInfo > Generic. Set MLB (Board Serial), SystemSerialNumber (Serial) and SystemUUID (SmUUID) to generated values. Change ROM to your network card's MAC address without the `:` character. [**How to get MAC Address?**](https://www.wikihow.com/Find-the-MAC-Address-of-Your-Computer)
5. Boot it!

## All work

- CPU
- Dual monitors (Displayport & HDMI & VGA)
- Audio
- Ethernet
- USB
- Wifi
- App store, iCloud, iMessage, iTunes, FaceTime, etc
- Sleep, Wakeup, Shutdown, Restart

## HIDPI fix

```bash
git clone https://github.com/xzhih/one-key-hidpi.git
cd one-key-hidpi
./hidpi.command
```
