---
sidebar_position: 5
---

# Resource download summary

## Hardware design

### 1.3 (Final prototype version)

- [v1.3 schematic pdf](https://dl.radxa.com/zero/docs/hw/RADAX_ZERO_V13_SCH_20210309.pdf) - Download Schematic for Radxa ZERO v1.3
- [v1.3 SMD pdf](https://dl.radxa.com/zero/docs/hw/RADAX_ZERO_V13_SMD_20210309.pdf) - Download Points Chart for Radxa ZERO v1.3

### 1.4 (First production version)

- [v1.4 schematic pdf](https://dl.radxa.com/zero/docs/hw/radxa_zero_v1400_schematic.pdf) - Download Schematic for Radxa ZERO v1.4
- [v1.4 SMD pdf](https://dl.radxa.com/zero/docs/hw/radxa_zero_v1400_smd.pdf) - Download Points Chart for Radxa ZERO v1.4
- [2D dxf for top and bottom](https://dl.radxa.com/zero/docs/hw/radxa_zero_v1400_2d.zip) - Download 2D CAD file for Radxa ZERO v1.4

Corrected footprint for TYPE-C connectors
Reduced footprint of ESD0402
Separated 1L2 and 1L4 to reduce the possibility of circuit shorting
Replaced FUSB340 with CH482
Power LED can now be controlled by GPIOAO_8
Therefore, pin 35 (GPIOAO_8) is not connected to the 40-pin header

### 1.5 (Fine tune)

Switch to other USB configuration channel controllers due to chip shortage

### 1.51 (Fine tune)

Power LED can now be controlled by GPIOAO_10
Therefore, pin 35 (GPIOAO_8) is now connected to the 40-pin header
Pin 38 (GPIOAO_10) is now not connected to the 40-pin header

## Flash Tools

- [Zagdig](https://zadig.akeo.ie/): Windows Maskrom Driver.
- [RZ USB Boot Helper](https://dl.radxa.com/zero/tools/windows/RZ_USB_Boot_Helper_V1.0.0.zip): Windows bootloader Load Tool.
- [factory-loader.img](https://dl.radxa.com/zero/images/loader/factory-loader.img): Used to erase eMMC on Windows. not recommended.
- [radxa-zero-erase-emmc.bin](https://dl.radxa.com/zero/images/loader/radxa-zero-erase-emmc.bin): Automatically erases the eMMC and then displays the eMMC as a USB storage device. This is the recommended method for burning Linux images.
- [rz-fastboot-loader.bin](https://dl.radxa.com/zero/images/loader/rz-fastboot-loader.bin): Enables fastboot mode, but cannot be used to install our official Android system.
- [android-bootloader.img](https://dl.radxa.com/zero/images/loader/android-bootloader.img): Same as bootloader.img in our official Android image. Some distributions use this bootloader.
- [rz-udisk-loader.bin](https://dl.radxa.com/zero/images/loader/rz-udisk-loader.bin): Embedded eMMC as a USB mass storage device.

## OS image

- [Radxa ZERO Debian Build 23](https://github.com/radxa-build/radxa-zero/releases/download/b23/radxa-zero_debian_bullseye_kde_b23.img.xz)

:::caution
Except for the above image which has been fully tested by the officials, the other mirrors have not been rigorously tested and may have unknown issues and are for evaluation use only.
:::

For more image, please check out： [Radxa ZERO Release](https://github.com/radxa-build/radxa-zero/releases)

- [Radxa ZERO Ubuntu Build 23](https://github.com/radxa-build/radxa-zero/releases/download/b23/radxa-zero_ubuntu_jammy_kde_b23.img.xz)
- [openSUSE Tumbleweed JeOS](http://download.opensuse.org/ports/aarch64/tumbleweed/appliances/openSUSE-Tumbleweed-ARM-JeOS-radxazero.aarch64.raw.xz)
- [Slarm64 Core (unofficial slackware)](http://dl.slarm64.org/slackware/images/radxa_zero/slarm64-current-aarch64-core-radxa_zero-6.4.8-build-20230806.img.zst)
- [Slarm64 Server (unofficial slackware)](http://dl.slarm64.org/slackware/images/radxa_zero/slarm64-current-aarch64-server-radxa_zero-6.4.8-build-20230806.img.zst)
- [Slarm64 XFCE (unofficial slackware)](http://dl.slarm64.org/slackware/images/radxa_zero/slarm64-current-aarch64-xfce-radxa_zero-6.4.8-build-20230806.img.zst)
- [Slarm64 Enlightenment (unofficial slackware)](http://dl.slarm64.org/slackware/images/radxa_zero/slarm64-current-aarch64-enlightenment-radxa_zero-5.14.5-build-20210917.img.zst)
- [CRUX-ARM](http://dl.slarm64.org/crux/images/radxa_zero/crux-arm-3.6-aarch64-core-radxa_zero-5.19.1-build-20220814.img.zst)
- [Manjaro Gnome](https://github.com/manjaro-arm/radxa-zero-images/releases/download/22.02/Manjaro-ARM-gnome-radxa-zero-22.02.img.xz)
- [Manjaro KDE](https://github.com/manjaro-arm/radxa-zero-images/releases/download/22.02/Manjaro-ARM-kde-plasma-radxa-zero-22.02.img.xz)
- [Manjaro Minimal](https://github.com/manjaro-arm/radxa-zero-images/releases/download/22.02/Manjaro-ARM-minimal-radxa-zero-22.02.img.xz)
- [Manjaro More Desktop Environment](https://github.com/manjaro-arm/radxa-zero-images/releases/tag/22.02)
- [TwisterOS Focal Beta5](https://drive.google.com/file/d/1T6GHK3DNbogkEXu7I7-kWqRdv7vltVDC/view?usp=sharing)

## Quality certification

- [CE RED - EU](https://dl.radxa.com/zero/docs/compliance/radxa_zero_ce_red_report.zip)
- [FCC ID - US](https://fccid.io/2A3PA-RADXA-ZERO)
