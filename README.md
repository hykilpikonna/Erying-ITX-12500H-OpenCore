# Erying ITX i5-12500H OpenCore

<img width="2043" alt="image" src="https://github.com/hykilpikonna/Erying-ITX-12500H-OpenCore/assets/22280294/bdacaaa1-4d7c-4eed-a8c3-2167f4945d12">

<img width="1284" alt="image" src="https://github.com/user-attachments/assets/e79e378e-892f-43be-a6c6-938df85093d6" />

OpenCore 1.0.3  
Tested on macOS 15.3 Sonoma

**!!!!IMPORTANT!!!!**

Before upgrading or installing macOS 14.4 and above, please edit the `config.plist` and set `SecureBootModel` to `Disabled`. ([Link](https://www.reddit.com/r/hackintosh/comments/1aevw0p/updating_to_144_beta_securebootmodel_disabled/))

**!!!!IMPORTANT!!!!**

The current version of OpenCore doesn't work with 12500H very well. It only passes the boot.efi handoff stage if you either disable Hyperthreading or disable all E-cores. In my testing, disabling Hyperthreading lead to better performance. (Track issue: https://github.com/dortania/bugtracker/issues/336)

## Hardware Configuration

| Part | Name | Price (+VAT) |
|:--:|:--|--:|
| MB  | Erying i5-12500H ITX (Taobao)                | ￥1369 CNY |
| RAM | 32GB (2 * 16) DDR4 3200 Samsung (Taobao)     | ￥252  CNY |
| GPU | AMD Vega 64 Reference Card (Kijiji)          | $100   CAD |
| SSD | WD Blue SN570 500GB (Canada Computers)       | $45    CAD |
| PSU | Lian Li SP 750 W 80+ Gold (Canada Computers) | $147   CAD |
| Fan | Jonsbo HX4170D (Taobao)                      | ￥139  CNY |
| Wifi | Intel AX210 (Taobao)                        | ￥73   CNY |
| Case | PCCooler i100 Pro (Taobao)                  | ￥277  CNY |
|  -  | + International Shipping EMS                 | ￥     CNY |
|  -  | = Sum                                        | =￥3686    |

## Peripherals

* Audio: ALC897
* Ethernet: RTL8125 + RTL8168/8111
* WiFi: Intel AX210
* Chipset: B660i

## Necessary BIOS Settings

* Disable Advanced > CPU > Hyperthreading
* Disable Advanced > Graphics > VT-d (Otherwise there will be a white square during boot stage)
* Disable Security > Secure Boot

## Features

- [ ] CPU Power Management (Not Tested)
- [x] NVRAM
- [x] AMD Graphics
  - [ ] DRM (Tested with Amazon Prime)
- [ ] Sleep/Wake (Low Priority)
  - [ ] Stay Asleep
  - [ ] Features Normal After Wake
- [x] 📶 2 Ethernet Adaptors (2.5G + 1G)
- [x] 📶 Intel AX210 Wifi & Bluetooth
  - [x] Wifi-6 Support 
- [ ] 🔌 USB Ports
- [x] 💬 iMessage
- [x] 🎧 Realtek ALC897 Audio

### Note on Wifi-6

Thanks to this guide on compiling itlwm with wifi6: https://github.com/OpenIntelWireless/itlwm/issues/897
