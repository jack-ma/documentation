---
sidebar_position: 2
---

import Etcher from '../../../common/general/\_etcher.mdx'

# 安装操作系统

## 准备工作

- 具有板载 eMMC 的 ZERO 主板
- Type-c 转 Type-a 数据线

## 镜像下载

请到[资源下载汇总](./download)下载对应的镜像文件

## 安装系统

1. 下载安卓镜像后解压。
2. 请参考[进入 maskrom 模式](../../low-level-dev/install-os-on-emmc#进入maskrom模式)。
3. 然后参考[擦除 eMMC ](../../low-level-dev/erase-emmc)加载[ android-bootloader.img ](https://dl.radxa.com/zero/images/loader/android-bootloader.img)，即可进入 fastboot 模式。
4. [下载并解压 android-platform-tools](https://developer.android.google.cn/tools/releases/platform-tools?hl=en)，并将路径添加到 PATH 环境变量。
5. Windows 系统运行 `./flash-all.bat` 脚本，Linux 系统运行 `./flash-all.sh` 脚本，即可开始刷写系统。

## 参考文档

- [从 USB OTG 口安装操作系统镜像到 eMMC](../../low-level-dev/install-os-on-emmc)
