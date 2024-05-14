<p align="center">
 <img src="https://github.com/zamkara/Lenovo-Thinkpad-X250-Hackintosh/raw/Opencore/screenshot/Banner.webp" align="center" alt="ROG-STRIX-G513QC" />
 <h2 align="center">Lenovo ThinkPad X250</h2>
 <p align="center">OpenCore Config for Lenovo ThinkPad X250 🍏</p>

<br><br>

<img src="https://github.com/zamkara/Lenovo-Thinkpad-X250-Hackintosh/raw/Opencore/screenshot/Screenshot%202024-02-14%20at%2018.19.56.png" alt="img" align="right" width="350px">
<br/><br/>

## Disclaimer ⚠️

This EFI is based in [olarila](https://olarila.com/files/OPENCORE1/EFI.Opencore.NoteBook.Broadwell.zip) and [exxncss](https://github.com/exxncss/x250-hackintosh) repository, go and support them. This repository couldn't be done without their work any suggestion is acepted to improve the files.
<br>

## Configuration  
| **Category**   | **Details**                               |
| -------------- | ------------------------------------------|
| CPU            | Intel Core i5-5300U                       |
| GPU            | Intel HD Graphics 5500                    |
| Memory         | Kingston 8GB DDR3L                        |
| Storage 1      | 256GB Midasforce M2.2242 SSD              |
| Storage 2      | 512GB Toshiba HDD Sata                    |
| Wifi           | Intel AC-7265 Dual Band + Bluetooth       |

</p>

## Screenshot
<p align="center">
  <kbd><br>V E N T U R A 13.6.4
  <br><br>
  <kbd><img src="https://github.com/zamkara/Lenovo-Thinkpad-X250-Hackintosh/raw/Opencore/screenshot/Screenshot%202024-02-14%20at%2005.50.22.png"/></kbd></kbd>
  <br><br>

> [!Warning]
> When installing or updating the system, be sure to make sure and replace some kext that matches your macOS version, otherwise, some components will not run properly.
<br>

<a href="https://github.com/zamprjkt/Lenovo-Thinkpad-X250-Hackintosh/releases" target="blank"><img align="left" width="300px" src="https://github.com/zamkara/Lenovo-Thinkpad-X250-Hackintosh/raw/Opencore/screenshot/download.svg" /></a>
Download the MacOS installation at the following link, [`Download Here`](https://www.olarila.com/topic/6278-new-vanilla-olarila-images/), Or download it from the macOS terminal directly by following this guide [`osxdaily`](https://osxdaily.com/2020/04/13/how-download-full-macos-installer-terminal/)
<br><br>

## ☑️ Tested
- sonoma (Tested, OpenCore, 8GB ram is highly discouraged)
- Ventura (Tested, OpenCore)
- Monterey (Tested, OpenCore)
- Bigsur (Tested, OpenCore)

## 🎒 Installation guide

### Monterey and below
- Clone this repo through the terminal.

    ```
    git clone https://github.com/zamkara/Lenovo-Thinkpad-X250-Hackintosh.git
    ```
- Download *Wireless Kernel Extension* from [Bluetooth](https://github.com/OpenIntelWireless/IntelBluetoothFirmware) & [itlwm](https://github.com/OpenIntelWireless/itlwm) then place it in the `$source/EFI/OC/Kexts` directory, be sure to download Airportitlwm for the appropriate macOS version or use itlwm for all macOS versions.
- Update the config to register the kext that was added to the folder using [OCAuxiliaryTools](https://github.com/ic005k/OCAuxiliaryTools) or [Opencore configurator](https://mackie100projects.altervista.org/download-opencore-configurator/).
- Place the EFI on the EFI Bootable partition of the macOS installer that was prepared earlier.
### Ventura and above


- The EFI I built cannot boot (used for installing the OS) on Ventura and later versions. It will only work when the system is patched using [OCLP](https://github.com/dortania/OpenCore-Legacy-Patcher). For the OS installation, you will need a different EFI from [Olarila](https://olarila.com).

- Download the [Olarila EFI](https://olarila.com/files/OPENCORE1/EFI.Opencore.NoteBook.Broadwell.zip) and add the Kexts from the released EFI in this repository. Don't forget to change the SMBIOS Model to a 2019 model or any other supported model.

- Perform the OS installation using the customized EFI, and apply the patch using [OCLP](https://github.com/dortania/OpenCore-Legacy-Patcher). Once done, replace the EFI with the one you can clone from this repository.
- After patching you can use the EFI from this repo for more functionality.

> You may encounter problems when granting certain permissions to apps on Ventura or above, I suggest you use [Allowme](https://github.com/zamkara/Allowme).

## Bios setup

- `Security -> Security Chip`: **Disabled**;
- `Memory Protection -> Execution Prevention`: **Enabled**;
- `Virtualization -> Intel Virtualization Technology`: **Enabled**;
- `Virtualization -> Vt-directed IO`: **Disabled**;
- `Internal Device Access -> Bottom Cover Tamper Detection`: must be **Disabled**;
- `Anti-Theft -> Computrace -> Current Setting`: **Disabled**;
- `Secure Boot -> Secure Boot`: **Disabled**;
- `UEFI/Legacy Boot`: **UEFI Only**;
- `CSM Support`: **No**.

## What's Working?
- QE/CI Intel HD Graphics 5500 `BigSur` `Monterey` `Ventura`
- Power Management `BigSur` `Monterey` `Ventura`
- Sleep, Shutdown, Restart `BigSur` `Monterey` `Ventura`
- Audio Speaker & Earphone `BigSur` `Monterey` `Ventura`
- Bluetooth `BigSur` `Monterey` `Ventura`
- Trackpad, Trackball, Gestures `BigSur` `Monterey` `Ventura`
- Indikator baterai `BigSur` `Monterey` `Ventura`
- Camera `BigSur` `Monterey` `Ventura`
- etc

## Credits:
- [Ikhsaan](https://github.com/exxncss)
- [Friction • RK800](https://t.me/gerobaksariroti)
- [Irawan](https://t.me/irawansalt)
