---
sidebar_position: 1
sidebar_class_name: hidden
---

# 安装系统到 EMMC

## 准备工作

- Radxa Zero
- 电脑（Windows，Linux或MacOS）
- USB A to C或 C to C的数据线

## 镜像下载

请到 [资源下载汇总](/rock5/rock5b/getting-started/download.md) 下载对应的镜像文件

## 进入Maskrom模式

首先在板子的背面找到USB boot button:
![Zero_usb_boot](/img/zero/zero/Zero_usb_boot.webp)

按住这个按键，将数据线插入电脑，直到电源灯亮了就松开。

在windows中的设备管理器，可以看到出现下面的设备
![Windows-GX-CHIP](/img/zero/zero/Windows-GX-CHIP.webp)

## 安装驱动

下载安装[Zagdig](https://zadig.akeo.ie/)软件安装USB驱动，如果在插入设备后没有出现下图中的设备信息，选择 `Options`->`List All Devices`

![Zagdig-libusb](/img/zero/zero/Zagdig-libusb.webp)

Windows下需要使用[RZ USB Boot Helper 工具](https://dl.radxa.com/zero/tools/windows/RZ_USB_Boot_Helper_V1.0.0.zip)软件从USB加载二进制文件，比如擦除eMMMC的操作。连接Radxa Zero进入Maskrom, RZ USB Boot Helper 工具没有显示 `Not detected, press and hold USB boot key and power on` 的提示就表示已经进入maskrom。接下来就可以进行[擦除eMMC](erase-emmc).

![Rz-usb-helper-maskrom](/img/zero/zero/Rz-usb-helper-maskrom.webp)

注意：擦除过程不要断开Radxa Zero的连接，直到电脑的资源管理器中出现一个大容量存储设备则表示擦除成功，可以进行新的镜像烧录。

## 安装系统到 eMMC

参考[安装操作系统](../getting-started/install-os#安装系统)，在选择要刷写存储设备时，选择 ZERO 模拟的大容量存储设备即可。

## 启动系统

- 给开发板上电，然后系统开始启动，状态灯闪烁。

:::tip
ZERO 支持 `5V` 供电。瑞莎推荐使用 [Radxa Power PD30W](../accessories/pd-30w)。
:::
