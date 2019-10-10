## 2018 Mac Mini Hackintosh

| Item | Spec |
|------|------|
|系统   | macOS 10.14.6 |
|处理器 | Intel Core i3-8100 @ 3.6GHz |
|主板   | Onda H310SD3-ITX |
|内存   | Onda 8G*2 DDR3-1600MHz |
|硬盘   | Intel 540s 360G M.2 Sata |
|显卡   | Intel UHD Graphics 630 |
|网卡   | CF-811AC USB WIFI |
|Clover| r4934 |

现状：目前声卡、网卡、硬解、睡眠、HWMonitor温度检测均正常。**可直接升级macOS 10.14.6 Mojave**。

## Releases Log

#### 20190620：稳定构建
  - 在tonymac tools安装和驱动安装完毕后，基于pcbeta某大神在config.plist中设定的dsdt patch，完成构建。
  - CF-811AC更小更便宜，官网新版的驱动都可以驱动，见`mac_utils/RTLWlanU_MacOS10.9_MacOS10.14_Driver_1830.20.b31_1827.4.b32_UI_5.0.8.b4.zip`，另[官方下载地址](http://www.comfast.cn/index.php?m=content&c=index&a=show&catid=30&id=335)
