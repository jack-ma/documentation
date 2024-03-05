---
sidebar_position: 4
---

# 硬件接口说明

<!-- 以下接口如果没有就删除，如果有的接口没有列出来，就加上去 -->

## 接口总览

- **ZERO**
  ![Radxa ZERO](/img/zero/zero/Zero_ports.webp)

## 处理器

ZERO 的 SoC 是 Amlogic S905Y2。CPU 为四核 ARM Cortex-A53 处理器。 搭载的 ARM G31 MP2 GPU 使 S905Y2 完全兼容 OpenGL ES 3.2, Vulkan 1.0 和 OpenCL 2.0。特殊 2.5D 硬件引擎将最大化显示性能并提供流畅的操作。

## 内存

ZERO 有一个 32 bits LPDDR 4 芯片。ZERO 提供 512MB、1GB、2GB 和 4GB 的内存选项。

## USB OTG（电源接口）

Radxa ZERO 被设计为低功耗的 ARM 单板计算机。它支持以下电源输入：  
Radxa ZERO 的功耗比较低，可以直接使用电脑USB供电，所以不再需要准备单独的电源适配器。如果独立使用Radxa ZERO，可以使用 5V，1A（至少）的电源适配器。  
使用电脑USB供电请使用USB3.0（可提供900mA电流），USB2.0只有500mA的电流会导致板子不稳定。  
此接口可用于连接键盘、鼠标、U盘等外设。

## TYPE-c USB3.0

此接口可用于连接键盘、鼠标、U盘等外设。

## 40 PIN GPIO

#### GPIO 电压

| GPIO       | 电压 | 最高 |
| ---------- | ---- | ---- |
| 所有的GPIO | 3.3V | 3.3V |

#### GPIO 接口

ZERO 提供了一个40 pin 针脚的 GPIO 座子，与市场上大多数的 SBC 配件兼容。

**提示：实际兼容情况以使用情况为准。**

<div className='gpio_style'>

:::caution
根据硬件版本的不同，引脚 35 和 38 其中一个引脚连接到了电源 LED，而不是连接到 40 引脚针座上。如果您的设计使用了这些引脚，请在购买前确认硬件版本。  
GPIOAO_8 和 GPIOAO_10 在 v1.51 及更高的硬件版本中可用。  
GPIOA_14 和 GPIOA_15 连接到了上拉电阻和 USB-C 控制器，因此不能用于一般 GPIO。  
引脚 22 (GPIOC_7) 和引脚 36 (GPIOH_8) 是开漏引脚。这意味着在用于输入时，它们需要连接到 GND 或 VCC（浮动状态未定义）；在用于输入时，它们需要外部上拉。除此之外，GPIOH_8 采用 5V 逻辑电平。
:::

| GPIO number |   Function4   |   Function3   |   Function2   | Function1  |               Pin#               |              Pin#               | Function1  |                  Function2                  |   Function3   |   Function4   | GPIO number |
| ----------- | :-----------: | :-----------: | :-----------: | :--------: | :------------------------------: | :-----------------------------: | :--------: | :-----------------------------------------: | :-----------: | :-----------: | ----------- |
|             |               |               |               |   +3.3V    | <div className='yellow'>1</div>  |  <div className='red'>2</div>   |   +5.0V    |                                             |               |               |             |
| 490         |               |               | I2C_EE_M3_SDA |  GPIOA_14  |  <div className='green'>3</div>  |  <div className='red'>4</div>   |   +5.0V    |                                             |               |               |             |
| 491         |               |               | I2C_EE_M3_SCL |  GPIOA_15  |  <div className='green'>5</div>  | <div className='black'>6</div>  |    GND     |                                             |               |               |             |
| 415         | I2C_AO_S0_SDA | UART_AO_B_RX  | I2C_AO_M0_SDA |  GPIOAO_3  |  <div className='green'>7</div>  | <div className='green'>8</div>  |  GPIOAO_0  | <div className='orange'>UART_AO_A_TXD</div> |               |               | 412         |
|             |               |               |               |    GND     |  <div className='black'>9</div>  | <div className='green'>10</div> |  GPIOAO_1  | <div className='orange'>UART_AO_A_RXD</div> |               |               | 413         |
| 414         | I2C_AO_S0_SCL | UART_AO_B_TX  | I2C_AO_M0_SCL |  GPIOAO_2  | <div className='green'>11</div>  | <div className='green'>12</div> |  GPIOX_9   |                 SPI_A_MISO                  |    TDMA_D0    |               | 501         |
| 503         |   TDMA_SCLK   | I2C_EE_M1_SCL |  SPI_A_SCLK   |  GPIOX_11  | <div className='green'>13</div>  | <div className='black'>14</div> |    GND     |                                             |               |               |             |
|             |               |               |               | SARADC_CH1 | <div className='green'>15</div>  | <div className='green'>16</div> |  GPIOX_10  |                  SPI_A_SS0                  | I2C_EE_M1_SDA |    TDMA_FS    | 502         |
|             |               |               |               |   +3.3V    | <div className='yellow'>17</div> | <div className='green'>18</div> |  GPIOX_8   |                 SPI_A_MOSI                  |     PWM_C     |    TDMA_D1    | 500         |
| 447         |               |  SPI_B_MOSI   | UART_EE_C_RTS |  GPIOH_4   | <div className='green'>19</div>  | <div className='black'>20</div> |    GND     |                                             |               |               |             |
| 448         |     PWM_F     |  SPI_B_MISO   | UART_EE_C_CTS |  GPIOH_5   | <div className='green'>21</div>  | <div className='green'>22</div> |  GPIOC_7   |                                             |               |               | 475         |
| 450         | I2C_EE_M1_SCL |  SPI_B_SCLK   | UART_EE_C_TX  |  GPIOH_7   | <div className='green'>23</div>  | <div className='green'>24</div> |  GPIOH_6   |                UART_EE_C_RX                 |   SPI_B_SS0   | I2C_EE_M1_SDA | 449         |
|             |               |               |               |    GND     | <div className='black'>25</div>  | <div className='green'>26</div> | SARADC_CH2 |                                             |               |               |             |
| 415         | I2C_AO_S0_SDA | UART_AO_B_RX  | I2C_AO_M0_SDA |  GPIOAO_3  |  <div className='blue'>27</div>  | <div className='blue'>28</div>  |  GPIOAO_2  |                I2C_AO_M0_SCL                | UART_AO_B_TX  | I2C_AO_S0_SCL | 414         |
|             |               |               |               |     NC     | <div className='green'>29</div>  | <div className='black'>30</div> |    GND     |                                             |               |               |             |
|             |               |               |               |     NC     | <div className='green'>31</div>  | <div className='green'>32</div> |  GPIOAO_4  |                   PWMAO_C                   |               |               | 416         |
|             |               |               |               |     NC     | <div className='green'>33</div>  | <div className='black'>34</div> |    GND     |                                             |               |               |             |
| 420         |               |               | UART_AO_B_TX  |  GPIOAO_8  | <div className='green'>35</div>  | <div className='green'>36</div> |  GPIOH_8   |                                             |               |               | 451         |
| 421         |               |               | UART_AO_B_RX  |  GPIOAO_9  | <div className='green'>37</div>  | <div className='green'>38</div> | GPIOAO_10  |                   PWMAO_D                   |               |               | 422         |
|             |               |               |               |    GND     | <div className='black'>39</div>  | <div className='green'>40</div> | GPIOAO_11  |                   PWMAO_A                   |               |               | 423         |

</div>

#### GPIO 编号

- GPIO 分为两组，即 GPIO AO 域和 GPIO EE 域  
  AO 域： GPIOAO_0 - GPIOAO_11  
  EE 域： GPIOA_14 - GPIOA_15 | GPIOH_0 - GPIOH_8 | GPIOX_0 - GPIOX_19
- UART  
  AO 域： UARTAO_A | UARTAO_B  
  EE 域： UART_A | UART_B | UART_C

| GPIO芯片 | GPIO名字 | 基础 | 偏移 |   计算公式    |
| :------: | :------: | :--: | :--: | :-----------: |
|  First   | GPIOAO_x | 412  | 0-11 | Base + Offset |
|  First   | GPIOE_x  | 424  | 0-2  | Base + Offset |
|  Second  | GPIOZ_x  | 427  | 0-15 | Base + Offset |
|  Second  | GPIOH_x  | 443  | 0-8  | Base + Offset |
|  Second  |  BOOT_x  | 452  | 0-15 | Base + Offset |
|  Second  | GPIOC_x  | 468  | 0-7  | Base + Offset |
|  Second  | GPIOA_x  | 476  | 0-15 | Base + Offset |
|  Second  | GPIOX_x  | 492  | 0-19 | Base + Offset |

## Micro HDMI

Radxa ZERO 板载一个micro HDMI的视频输出接口，需要使用micro HDMI 转标准HDMI 线连接显示器。  
HDMI的输出分辨率取决于显示器，Radxa ZERO会根据显示器调整到最佳的显示分辨率。

## eMMC

板载的eMMC是板子背面的那个大的贴片芯片，用于 eMMC 启动或数据存储。我们提供从无到 128GB 的选项。

## WIFI/BT

ZERO板载了一个 WIFI/BT 模块，可用于连接 WIFI 和蓝牙

## MicroSD 卡槽

用于 MicroSD 卡启动或数据存储。

## USB BOOT 按钮

ZERO 支持 USB 镜像下载烧录模式，这是将 eMMC 映射为 USB 存储设备的一种特殊操作模式。  
当需要把镜像写到eMMC 上时，需要使用 USB BOOT 按钮进入 USB 镜像下载烧录模式。
