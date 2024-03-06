---
sidebar_position: 1
---

# 准备工作

## 开发准备

<!-- 下面不需要的设备，可以删除 -->

### 电源

ZERO 采用 Type-C 接口供电，输入电压为5V。  
推荐使用官方的 Radxa Power PD 30W 。<img src="/img/accessories/pd-30w.webp" alt="Radxa Power PD 30W" width="300" />

### 启动介质

板载的eMMC 或 sd卡  
如果开发板没有板载eMMC则需要准备一个至少8GB的sd卡. [eMMC位于开发板背面](../../hardware-design/hardware-interface#接口总览)，您可以检查一下您的开发板是否具有这个元件。  
如果需要安装带有桌面环境的镜像，请使用至少16GB的sd卡，推荐使用32GB。

### microSD 读卡器

用于烧录系统镜像。

### 显示器

Radxa ZERO 板载一个micro HDMI的视频输出接口，需要使用micro HDMI 转标准HDMI 线连接显示器。  
HDMI的输出分辨率取决于显示器，Radxa ZERO会根据显示器调整到最佳的显示分辨率。

### 网络连接

ZERO 板载一个 ap6212/ap6256/aw-cm256sm WiFi/BT 模块。

### Type-C Hub

Radxa ZERO 有一个板载 [Type-C USB3.0接口](../../hardware-design/hardware-interface#接口总览)。这个接口支持通过 USB Type-C hub 转出 Type-A 口和有线网(如果 hub 支持)，但是不具备视频输出功能。

### USB 鼠标和键盘

可以通过接在USB Hub上的键鼠控制Radxa ZERO。

## 参考文档

[支持的配件](../../accessories)
