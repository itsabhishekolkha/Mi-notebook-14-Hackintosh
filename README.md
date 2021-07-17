# macOS  on Mi NoteBook 14

![image](https://user-images.githubusercontent.com/77840685/121693914-33c90400-cae7-11eb-8285-576b83f1598c.png)

#### This repo is currently compatible with macOS Big Sur and Catalina
|     macOS Big Sur      |     macOS Catalina     |   macOS monterey      |      
|------------------------|------------------------|-----------------------|
|     11.4   (20F71)     |     10.15.7  (19H15)   |  12.0(Beta) 21A5248P  |
|     11.3.1 (20E241)    |     10.15.6  (19G2021) |                       |
|     11.3   (20E232)    |     10.15.5  (19F101)  |                       |   
|     11.2.3 (20D91)     |     10.15.4  (19E287)  |                       |
|     11.2.2 (20D80)     |     10.15.3  (19D76)   |                       |
|     11.2.1 (20D74)     |     10.15.2  (19C57)   |                       | 
|     11.2   (20D64)     |     10.15.1  (19B88)   |                       |   
|     11.1   (20C69)     |     10.15    (19A583)  |                       |
|     11.0.1 (20B29)     |                        |                       |



### DISCLAIMER
* For best results, read the entire README before you start and follow the install instruction throughly.
* I am not responsible for any damages you may cause.
* Should you find an error or improve anything — whether in the config or in the documentation — please consider opening an issue or pull request.
* Please do not **clone or download** the main branch for daily use: it may include u**nstable code** just because it is my repository.

* If you find this bootloader configuration useful, consider **giving** it **a star** to make it more visible.
* If you find my work useful, please consider Give me a **Star** and follow me on **GitHub**:heart:

### Introduction
This repo contains information for getting macOS working on a **mi NoteBook 14** (all Edition) laptop.ive 

This is intended to create a "fully" functional (as far as possible) hackintosh for the Mi noteBook 14. If you would like to get started with creating a hackintosh on your Mi NoteBoook 14 but have non experience, I would highly recommend following [Dortania's OpenCore Install guide](https://dortania.github.io/OpenCore-Install-Guide/) and then returning here for troubleshooting. With each new release of macOS we need to resolve each new "minor issue" we run into. The installation is not perfect yet since it's a continuos work-in-progress, but I'm glad to say that **I learned a lot in the meantime**. All of the steps I made to get to this point were a result of countless hours of reading along with trial and error. I am by no means an expert so any help to get this project functional is very appreciated!

### Summary

* The **compatibility** is **very good** for the most part, most of the stuff works like it would on a real MacBook, including camera, audio, touchpad, iCloud services.
* The **experience** is **pleasant**, as the laptop is smooth and responsive under macOS Big Sur.
* **Battery life** is **quite great** (from personal experience it lasts from **7 to 8 hours** for light works depending on its age with a behaviour very similar to Windows 10 as shown in the macOS menu bar screenshots below).
* The **Intel WiFi** card can be replaced with a Broadcom one, but the Intel card is now **functional albeit not operating at full speeds** (however it is fine for most use cases). With the latest `AirportItlwm.kext` even **Handoff** and **Continuity** features are working, but with a very limited support for AirDrop and Apple Watch unlocking (see [Changelog for OpenIntelWireless release v. 1.2.0 stable](https://github.com/OpenIntelWireless/itlwm/releases)).
For any issues about `AirportItlwm.kext` please refer first to [**OpenIntelWireless Troubleshooting page**](https://openintelwireless.github.io/itlwm/Troubleshooting.html#kernel-extension-loading-status) and then to [**OpenIntelWireless Gitter Page**](https://gitter.im/OpenIntelWireless/itlwm?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

![image](https://user-images.githubusercontent.com/77840685/121717499-de98ec80-cafe-11eb-97c1-dff7d27d1848.png)

**This repository is for personal purposes**


## YouTude Guide For Installing

* [Installing Video Guide](https://youtu.be/4LgyTZQ3jfQ)
* You can follow this guide to install MacOS In your Mi Notebook 14.
* Don't forgot to subscribe...it means a lot me.:D


### Generate your own SMBIOS Information


For privacy reasons, all SMBIOS information has been wiped out in the configuration file `EFI/OC/config.plist`. You need to generate your unique `SMBIOS` info by yourself (recommend to use [**CorpNewt's GenSMBIOS**](https://github.com/corpnewt/GenSMBIOS)), and inject them into your `config.plist`.
- With every **EFI update** you retrieve from [here](https://github.com/itsabhishekolkha/Mi-notebook-14-Hackintosh), please, remember to transfer your Device details under `PlatformInfo -> Generic` in your `config.plist`.

<img width="698" alt="AboutThisMac" src="https://user-images.githubusercontent.com/77840685/121720983-5bc56100-cb01-11eb-9a6c-492e033b347f.png">

# Configuration

| Specification | Details                                         |
| ------------- | ------------------------------------------------|
| Model         |   Mi notebook 14                                |     
| Processor     |    intel core (i3-10110U/ i5-10210U/ i7-10510U) |
| Generation.   | 10th Gen. Comet Lake                            |
| Memory        | 8GB 2666MHz DDR4 RAM                            |
| Storage       |SATA 3 SSD, NVMe SSD                             |
| Graphics      | Integrated intel UHD,~~NVIDIA® GeForce® MX350~~ |
| Sound card    | Realtek ALC256(layout-id: 88)                   | 
| Wireless card | intel Wireless AC 9462                          |
| Trackpad      |I2C ELAN2304                                     |

### Status
- [x] **Intel UHD 620** Graphics card
- [x] **Intel Wifi**
- [x] **Bluetooth**
- [x] **Audio** Streo/Mono sound using **headphone jack**
- [x] **Battery** status
- [x] **Keyboard** working with all **functions**(Alt=command, windows= Option etc.)
- [x] **Touchpad** working with all **gestures**
- [x] **HandOff**
- [x] **Sleep**
- [x] **Camera**
- [x] **Face Time and imessage** will work after SMBIOS edit.
- [x] **Mic** Will working... Follow the guide below.
- [x] **HDMI** up to two 4K @60 Hz monitors
- [x] **Native Color Profile**

## Repo Updates
    This repo is currently compatible with macOS Big Sur & catalina.


*    OpenCore Updates
*     0.7.0 Updated
     
*    **EFI** tested on 
*       Mi Notebook 14 10th Generation Intel® Core™ i5(Intel® UHD Graphics 620)
        Mi NoteBook 14 e-Learning Edition 10th Generation Intel® Core™ i3(Intel® UHD Graphics 620)
*     Fri 17 Jun 2021

## OpenCore

* Current OpenCore version of **EFI** is-
*     OpenCore 0.7.0

### Benchmark Tests

* **CPU**(Performance of CPUs at performing everydays task.)

![image](https://user-images.githubusercontent.com/77840685/121767659-3c691b00-cb77-11eb-8377-f627e84367ea.png)
 
* **Compute**(Performance of GPUs at performing common compute task.)

![image](https://user-images.githubusercontent.com/77840685/121767702-9073ff80-cb77-11eb-8fe0-6570506de890.png)
 
## Post - Install Settings
<details>
<summary><strong>Enable Tap (with one finger) for Touchpad</strong></summary>

Starting from [VoodooI2C v. 2.4.1](https://github.com/VoodooI2C/VoodooI2C/releases), the **click down** action is emulated to **force touch**, which causes the failure of click down and drag gestures.

For example, you can turn off `Force Click` in `System Preferences -> Trackpad` or choose three finger drag in `System Preferences -> Accessibility -> Mouse & Trackpad -> Trackpad Options`

Suggested configuration:
    
![image](https://user-images.githubusercontent.com/77840685/121724879-253e1500-cb06-11eb-9576-2f4843ec79db.png)
</details>

<details>
<summary><strong>Enable Apple Services</strong></summary>

Default **SMBIOS** settings of this repo is `MacBookPro16,3` ~~`MacBookPro14,1`~~ ~~`MacBookPro15,2`~~
1. Launch `Terminal` app
2. Copy the following script, paste it into the `Terminal` window, then press `Enter`
   ```bash
   git clone https://github.com/corpnewt/GenSMBIOS && cd GenSMBIOS && ./GenSMBIOS.command 
   ```
3. Type `2`, then press `Enter`
4. Drag your `config.plist` inside the `Terminal` window
5. Type `3`, then press `Enter`
6. Type `MacBookPro16,3`, then press `Enter`
</details>

<details>
    <Summary><strong>Microphone Fix</strong></summary>

Download [Combojack.](https://github.com/hackintosh-stuff/ComboJack)

* Follow given documentation to install combojack.
* Go to system Preferences > Sound > Input and choose Line In as input device.
* Insert headphone, combojack pop-up will appear, select headset from the list.
* If you still face any issue disable ambient noice cancellation.
* you are good to go.
</details>

<details>
    <Summary><strong>MacOS HiDPI</strong></summary>

MacOS HiDPI [Click Here.](https://github.com/xzhih/one-key-hidpi)
</details>

<details>
<summary><strong>Booting MacOS without installer pendrive</strong></summary>

[Click Me](https://www.youtube.com/watch?v=qmYEQoFRFH0&list=LL&index=1)
    </details>

<details>
    <Summary><strong>Mi NoteBook 14 Colour Profile</strong></summary>
    
   ### Installation
    
- Run the following command in Terminal-
(sh -c "$(curl -fsSL https://raw.githubusercontent.com/daliansky/XiaoMi-Pro-Hackintosh/main/ColorProfile/one-key-colorprofile.sh)

- Or you can manually put the color profile into /Library/ColorSync/Profiles/

- Open System Preferences -> Displays -> Color

- Select NV156FHM-N61 profile

- Reboot
    </details>

## Update tracker

| Item | Version | Remark |
| :--- | :--- | :--- |
| MacOS | 11.4 | |
| [OpenCore](https://github.com/acidanthera/OpenCorePkg/releases) | 0.7.0 | Default Bootloader|
| [Lilu](https://github.com/acidanthera/Lilu/releases) | 1.5.3 | Kext/process/framework/library patcher |
| [WhateverGreen](https://github.com/acidanthera/whatevergreen/releases) | 1.4.9 | Handle Graphics card |
| [AppleALC](https://github.com/acidanthera/AppleALC/releases) | 1.6.0 | Handle/fix onboard audio |
| [CodecCommander](https://github.com/Sniki/EAPD-Codec-Commander/releases) | 2.7.2 | Fix headphone audio switch |
| [CPUFriend](https://github.com/acidanthera/CPUFriend/releases) | 1.2.3 | Power management |
| [HibernationFixup](https://github.com/acidanthera/HibernationFixup/releases) | 1.4.0 | Handle hibernate status |
| [IntelBluetoothFirmware](https://github.com/OpenIntelWireless/IntelBluetoothFirmware/releases) | 1.1.2 | Handle Bluetooth |
| [AirportItlwm](https://github.com/OpenIntelWireless/itlwm/releases) | 2.0.0 beta| Handle native Wi-Fi card |
| [NullEthernet](https://bitbucket.org/RehabMan/OS-X-Null-Ethernet/downloads/) | 1.0.6 | Fake Ethernet card |
| [NoTouchID](https://github.com/al3xtjames/NoTouchID/releases) | 1.0.4 | Disable TouchID|
| [NVMeFix](https://github.com/acidanthera/NVMeFix/releases) | 1.0.7 | Fix for NVMe SSDs |
| [RestrictEvents](https://github.com/acidanthera/RestrictEvents/releases) | 1.0.1 | Block unwanted processes |
| [VoodooI2C](https://github.com/alexandred/VoodooI2C/releases) | 2.5.2 | Handle I2C device |
| [VoodooI2CHID](https://github.com/alexandred/VoodooI2C/releases) | 2.5.2 | Touchpad I2C satellite |
| [VoodooPS2Controller](https://github.com/acidanthera/VoodooPS2/releases) | 2.2.3 | Enable keyboard, alternative trackpad driver |
| [VirtualSMC + plugins](https://github.com/acidanthera/VirtualSMC/releases) | 1.2.3 | SMC chip emulation |
| [USBInjectAll](https://github.com/daliansky/OS-X-USB-Inject-All/releases) | 0.7.6 | Inject USB ports |

# Credits

* Huge thanks to [Profzie](https://github.com/profzei/Matebook-X-Pro-2018)
* Thanks to [Daliansky and stevezhengshiqi](https://github.com/daliansky/)
* Thanks to [Dortania](https://dortania.github.io/OpenCore-Install-Guide/prerequisites.html#prerequisites)
* Thanks to [Acidanthera](https://github.com/acidanthera) for providing [AppleALC](https://github.com/acidanthera/AppleALC), [HibernationFixup](https://github.com/acidanthera/HibernationFixup), [Lilu](https://github.com/acidanthera/Lilu), [NVMeFix](https://github.com/acidanthera/NVMeFix), [OcBinaryData](https://github.com/acidanthera/OcBinaryData), [OpenCorePkg](https://github.com/acidanthera/OpenCorePkg), [RestrictEvents](https://github.com/acidanthera/RestrictEvents), [VirtualSMC](https://github.com/acidanthera/VirtualSMC), [VoodooInput](https://github.com/acidanthera/VoodooInput), [VoodooPS2](https://github.com/acidanthera/VoodooPS2), and [WhateverGreen](https://github.com/acidanthera/WhateverGreen).
* Thanks to [OpenIntelWireless](https://github.com/OpenIntelWireless) for providing [AirportItlwm](https://github.com/OpenIntelWireless/itlwm) and [IntelBluetoothFirmware](https://github.com/OpenIntelWireless/IntelBluetoothFirmware).
* Thanks to [RehabMan](https://github.com/RehabMan) for providing [OS-X-Clover-Laptop-Confi(OS-X-Clover-Laptop-Config), [OS-X-Null-Ethernet](https://github.com/RehabMan/OS-X-Null-Ethernet), and [SATA-unsupported](https://github.com/RehabMan/hack-tools/tree/master/kexts/SATA-unsupported.kext).
* Thanks to [Sniki](https://github.com/Sniki) for providing [EAPD-Codec-Commander](EAPD-Codec-Commander).
* Thanks to [VoodooI2C](https://github.com/VoodooI2C) for providing [VoodooI2C](https://github.com/VoodooI2C/VoodooI2C).
* Thanks to [ComboJack.](https://github.com/hackintosh-stuff/ComboJack)
* Last but not least Thanks to [Me.](https://github.com/itsabhishekolkha/)
