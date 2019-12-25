## iMac (Retina 4K, 21.5-inch, 2019) Hackintosh

| Item | Spec |
|:------|:------|
|系统   | macOS 10.15.2 Catalina + Windows 10 |
|处理器 | Intel Core i3-8100 @ 3.6GHz |
|主板   | MSI B360M Fire |
|内存   | Corsair 8G*2 2400MHz DDR4 |
|硬盘   | Intel 760P 256G M.2 NVMe SSD + WD 1T HDD |
|显卡   | Yeston Radeon RX570 4G GDDR5|
|网卡   | 板载 Realtek RTL8111H + CF-915AC USB WiFi |
|声卡   | Realtek® ALC887 Codec |
|BIOS版本| 7B53v14 |
|Clover版本| r5100 |

### 硬件说两句：
- CPU：2018年发布的Intel 8代core i3，性能得到了相当的提升。4核@3.6GHz的i3-8100，日常办公影音空闲率在50%以上，性能上够用，TDP 65W散热基本问题不大。
- 显卡：10.14以后，免驱的就是AMD的RX系列和Nvidia的老系列卡了，选了盈通570，理论上可以4K。装个双系统的话，可以在Windows下面打打Steam小游戏。
- 主板+存储：微星品牌还是可以的，B360m Fire是22*18的MATX主板，作为主力机没问题，选用了Intel 760P这款兼容性好的SSD。
- WIFI：选用了USB WIFI CF-811AC/CF-915AC，10.13下免驱，Mojave和Catalina建议使用开源的[Wireless USB Adapter Clover](https://github.com/chris1111/Wireless-USB-Adapter-Clover/releases)软件，因为官方驱动是32位的。


## Releases Log

#### 20191212: 升级到Catalina 10.15.2

#### 20191128: Patch For USB 3.0 Devices
  - USB 3.0 优盘插到3.0口子不能用的bug，使用了USB Port Limit Patch修复。

#### 20191101: 升级到10.15.1
  - 升级AppleALC到1.4.3, Lilu到1.3.9, WhateverGreen到1.3.4，都是最新版；直接系统升级

#### 20191009：升级到10.15
  - 使用Clover Configurator升级Clover版本从4934到5070.
  - 使用Clover Configurator升级AppleALC.kext、WhateverGreen.kext到最新
  - OTA系统更新升级到Catalina正式版

#### 20190824：升级到10.14.6
  - 升级了3个kext驱动，直接系统更新到10.14.6

#### 20190610：升级Clover，主题精简
  - 使用Multibeast-11.3.0升级clover到r4934
  - 主题仅保留一个最简的Minimalism主题

![](EFI/CLOVER/themes/Minimalism/screenshot.png)

#### 20190519：新增硬件检测
  - 新增Apps文件夹，存放硬件检测软件
  - 新增HWMonitor和相关的kexts，主要是为了看温度
  - CPU-S, intel(R) Power Gadge查看系统cpu变频之类的
  - VideoProc查看硬件解码，通过
  - fliqlo为流行的时钟主题
  - RTLWlanU_*_Driver为USB WIFI的驱动。

#### 20190519：直接升级到mojave10.14.5
  - 基于Multibeast 11.2.0构建，Clover版本为r4920，支持macOS10.14.5；
  - kexts都已更新；
  - 网络问题导致直接安装报错，于是下载macos combo更新来直接安装，基本无人值守可以自行安装完成；
  - 更新细节：更新中会有一个新的 `Install MAC` clover boot选项，更新中会自动进入这个2次吧，最后这个选项消失，更新就完成了；然后CLover boot选项会变得和之前一样。

#### 20190517：修复无法预览jpg图片错误
预览要集成显卡的硬解功能
  - 我的i3-8100有集成显卡的，于是在bios里面开启igpu就可以了。
  - 网上的教程是把smbios改成不带集成显卡的机器，然后用NoVPAJpeg.kext来fix。

#### 20190517：修复shutdown reboots(关机重启)错误
  - BIOS降级: 请使用7B53v14或者13版本的bios，再高会出现问题，亲测。
  - 进入/EFI/CLOVER/drivers64UEFI；删除AptioMemoryFix-64.efi，添加OsxAptioFix2Drv-free2000.efi 和 EmuVariableUefi-64.efi；同时修改config.plist的boot模块添加slide=0。
