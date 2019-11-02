
[![996.icu](https://img.shields.io/badge/link-996.icu-red.svg)](https://996.icu)
[![LICENSE](https://img.shields.io/badge/license-Anti%20996-blue.svg)](https://github.com/996icu/996.ICU/blob/master/LICENSE)

个人使用和维护的几个Hackintosh Machine EFI，分享给有需要的朋友。

## 我是如何从零开始安装Hackintosh的
1. 入门：基于tonymacx86论坛的Install Guide，使用Unibeast制作安装U盘，使用Multibeast完成Post Install的驱动安装和config配置。
2. **使用须知**：请使用CLover Configurator替换一个新的SMBIOS。否则多个机器使用同一个硬件ID，可能会被苹果封锁。
3. 一些技术细节：
    - 这几个EFI没有做集成显卡id的注入、ssdt/dsdt等定制，通用性好一点。
    - Clover：是用来引导MacOS系统的，可以同时引导Windows和MacOS双系统。每代MacOS系统更新一般都需要把Clover升级到较新的版本才能无缝OTA升级。可参考[某B站视频](https://www.bilibili.com/video/av49751074?t=72)。
    - CLover Configurator：即CCG，通过plist文件配置引导细节，更新Clover和kexts驱动。一般要先加载EFI所在分区，也可以用`diskutil list`查看引导所在EFI分区。
    - Multibeast：系统安装上后，做kexts驱动适配用。默认会把kexts安装到/Library/Extensions/(/L/E)系统目录，为了系统更新后kexts不丢失，我把所有kexts驱动搬迁到/EFI/CLOVER/Kexts/other目录，即驱动和引导放在一起。
    - kexts缓存重建：有时候需要进行重建，可以解决一些开机起不来之类的问题；可以用指令`sudo kextcache -i /`操作，我看日志和网上有很多用Kext Utility操作的很像。
4. mac_utils辅助工具
    - neofetch: 查看系统spec
    - 查看cpu核心数: `sysctl hw.physicalcpu`, `sysctl hw.logicalcpu`
    - 查看空余内存: `alias free="top -l 1 -s 0 | grep PhysMem"`
    - HWSensors.6.26.1800.zip: kexts和app结合的硬件温度和使用情况的状态栏监测工具，仅适用于Hackintosh。我习惯用这个。
    - iStatusMenus: 另一个收费状态栏监测工具。文件夹有一些"好定西"。
    - Office 2019: 大家都懂的。
    - fliqlo: 时钟屏保。
    - CPU-S: 变频测试。
    - IntelPowerGadget: Intel官方硬件监测软件。
    - EW-7811Un_Mac_driver_v1.0.1.4.zip: CF-915AC USB WiFi驱动程序(新版本的驱动都无法稳定支持5G)，适用于Mojave及以前。Catalina需使用 [Wireless USB Adapter-V6.zip](https://github.com/chris1111/Wireless-USB-Adapter/releases)。
    - RTLWlanU_MacOS10.9_MacOS10.14_Driver*.zip: CF-811AC USB WiFi驱动程序，适用于Mojave及以前。贴[官方下载地址](http://www.comfast.cn/index.php?m=content&c=index&a=show&catid=30&id=335)

## My Hackintosh Machines：
#### iMac (Retina 4K, 21.5-inch, 2019)
![](./iMac-4k-2019-Catalina-10.15.1.png)


#### 2018 Mac Mini
![](./L65_itx_case.png)

```
                    'c.          shm@macmini.local
                 ,xNMM.          -----------------
               .OMMMMo           OS: macOS Mojave 10.14.6 18G87 x86_64
               OMMM0,            Host: Hackintosh (SMBIOS: Macmini8,1)
     .;loddo:' loolloddol;.      Kernel: 18.7.0
   cKMMMMMMMMMMNWMMMMMMMMMM0:    Uptime: 7 mins
 .KMMMMMMMMMMMMMMMMMMMMMMMWd.    Packages: 44 (brew)
 XMMMMMMMMMMMMMMMMMMMMMMMX.      Shell: bash 3.2.57
;MMMMMMMMMMMMMMMMMMMMMMMM:       Resolution: 1920x1080
:MMMMMMMMMMMMMMMMMMMMMMMM:       DE: Aqua
.MMMMMMMMMMMMMMMMMMMMMMMMX.      WM: Quartz Compositor
 kMMMMMMMMMMMMMMMMMMMMMMMMWd.    WM Theme: Blue (Light)
 .XMMMMMMMMMMMMMMMMMMMMMMMMMMk   Terminal: iTerm2
  .XMMMMMMMMMMMMMMMMMMMMMMMMK.   Terminal Font: Monaco 12
    kMMMMMMMMMMMMMMMMMMMMMMd     CPU: Intel i3-8100 (4) @ 3.60GHz
     ;KMMMMMMMWXXWMMMMMMMk.      GPU: Intel UHD Graphics 630
       .cooc,.    .,coo:.        Memory: 6515MiB / 16384MiB
```

#### MacBook Pro (Retina, 13-inch, Early 2015)
```
                    'c.          szymon@macbook2015.local
                 ,xNMM.          ------------------------
               .OMMMMo           OS: macOS Mojave 10.14.6 18G87 x86_64
               OMMM0,            Host: Hackintosh (SMBIOS: MacBookPro12,1)
     .;loddo:' loolloddol;.      Kernel: 18.7.0
   cKMMMMMMMMMMNWMMMMMMMMMM0:    Uptime: 9 mins
 .KMMMMMMMMMMMMMMMMMMMMMMMWd.    Packages: 42 (brew)
 XMMMMMMMMMMMMMMMMMMMMMMMX.      Shell: bash 3.2.57
;MMMMMMMMMMMMMMMMMMMMMMMM:       Resolution: 1600x900
:MMMMMMMMMMMMMMMMMMMMMMMM:       DE: Aqua
.MMMMMMMMMMMMMMMMMMMMMMMMX.      WM: Quartz Compositor
 kMMMMMMMMMMMMMMMMMMMMMMMMWd.    WM Theme: Blue (Light)
 .XMMMMMMMMMMMMMMMMMMMMMMMMMMk   Terminal: iTerm2
  .XMMMMMMMMMMMMMMMMMMMMMMMMK.   Terminal Font: Monaco 12
    kMMMMMMMMMMMMMMMMMMMMMMd     CPU: Intel i5-5300U (4) @ 2.30GHz
     ;KMMMMMMMWXXWMMMMMMMk.      GPU: Intel HD Graphics 5500
       .cooc,.    .,coo:.        Memory: 4841MiB / 16384MiB
```