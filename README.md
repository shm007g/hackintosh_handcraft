
[![996.icu](https://img.shields.io/badge/link-996.icu-red.svg)](https://996.icu)
[![LICENSE](https://img.shields.io/badge/license-Anti%20996-blue.svg)](https://github.com/996icu/996.ICU/blob/master/LICENSE)

个人使用的几个Hackintosh Machine，分享给有需要的朋友。

**使用须知**：请使用Clover Configurator替换一个新的SMBIOS以“洗白”；另外，多账户多机器使用同一个硬件ID，**可能会被苹果封锁AppleID**。

```
Office Desktop       : i3-8100, Onda H310 ITX, 8G*2 DDR3 Onda, Intel 540s M.2 Sata, macOS10.14.6
Laptop               : Thinkpad T450, i5-5300u, 8G*2 DDR3L, macOS10.14.6, mSata 256G
Home Desktop(former) : i3-8100, MSI B360M Fire, 8G*2 DDR4 corsair, Yeston RX570 4G, Intel 760p M.2 NVMe, macOS10.15.2 (**deprecated**)
Home Desktop(former) : Dell 9020m, i5-4670T, 4G*2 DDR3L Samsung, Samsung 850 EVO, macOS10.15.2 (**deprecated**)
```

### mac_utils 文件夹
- HWSensors.6.26.1800.zip: kexts和app结合的硬件温度和使用情况的状态栏监测工具，仅适用于Hackintosh。我习惯用这个。
- iStatusMenus: 另一个可破解的状态栏监测工具。
- Office 2019及“工具”包。
- fliqlo: 时钟屏保最新版。
- CPU-S: 变频测试。
- IntelPowerGadget: Intel官方硬件监测软件。
- neofetch: 查看系统spec
- 查看cpu核心数: `sysctl hw.physicalcpu`, `sysctl hw.logicalcpu`
- 查看空余内存: `alias free="top -l 1 -s 0 | grep PhysMem"`

### 如何从零开始安装Hackintosh
1. 入门：基于tonymacx86论坛的[Install Guide](https://www.tonymacx86.com/threads/unibeast-install-macos-mojave-on-any-supported-intel-based-pc.259381/)，配置好BIOS后，使用Unibeast制作安装U盘，使用Multibeast完成Post Install的驱动安装和config配置。
1. 一些技术细节：
    - 常识：安装一般很简单，打驱动可能会很麻烦；笔记本一般比台式机麻烦多很多。找贴近官方设备的硬件，借用已构建好的EFI比较省事。
    - Clover：是用来引导MacOS系统的，可以同时引导Windows和MacOS双系统。每代MacOS系统更新一般都需要把Clover升级到较新的版本才能无缝OTA升级。升级可参考[某B站视频](https://www.bilibili.com/video/av49751074?t=72)。
    - CLover Configurator：即CCG，通过plist文件配置引导细节，更新Clover和kexts驱动。一般要先加载EFI所在分区，也可以用`diskutil list`查看引导所在EFI分区。
    - kexts：硬件驱动程序。Multibeast默认会把kexts安装到/Library/Extensions/(/L/E)系统目录，为了系统更新后kexts不丢失，我把所有kexts驱动搬迁到/EFI/CLOVER/Kexts/other目录，即驱动和引导放在一起。
    - kexts缓存重建：kexts更新后可以用指令`sudo kextcache -i /`操作刷新驱动缓存。
