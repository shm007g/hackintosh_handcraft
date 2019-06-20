## Hackintosh Build: MBP 13 2015

```
                    'c.          szymon@macbook2015.local
                 ,xNMM.          ------------------------
               .OMMMMo           OS: macOS Mojave 10.14.5 18F132 x86_64
               OMMM0,            Host: Hackintosh (SMBIOS: MacBookPro12,1)
     .;loddo:' loolloddol;.      Kernel: 18.6.0
   cKMMMMMMMMMMNWMMMMMMMMMM0:    Uptime: 1 hour, 52 mins
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
       .cooc,.    .,coo:.        Memory: 5475MiB / 16384MiB
```

|hardware|spec|
|-|-|
|系统| MacOS 10.14.5 + Windows 10 |
|品名| ThinkPad T450 |
|处理器| Intel Core i5-5300u @ 2.3GHz |
|内存| 8*2 G DDR3-1600 |
|硬盘| BIWIN msata 256G + 500G HDD |
|显卡| Intel HD Graphics 5500 1536 MB|
|无线网络| CF-915AC/CF-811AC USB WIFI |
|声卡| Realtek® ALC3232 Codec |
|CLOVER| r4934 |

- 现状：目前网卡、硬解、睡眠、HWMonitor温度检测均正常；耳机孔爆音，外接vga无法使用。
- 鱼：基于pcbeta大神提供的e450 ssdt搭建，最新的Clover和kexts驱动，支持直接升级macos10.14.5。
- 渔：基于tonymac的install guide，使用unibeast和multibeast构建，配合以上ssdt。
  - multibeast原生会把kext安装到/L/E下面，为了保持kexts的稳定性，我建议把所有驱动搬迁到/EFI/CLOVER/Kexts/$(version)下面去，让驱动和引导放在一起；
  - 调整kexts后最好重建下kext缓存，以免开机起不来之类的；操作指令`sudo kextcache -i /`。网上有很多用Kext Utility操作的，我看日志应该和kextcache操作一样。
- 使用建议：相似硬件的朋友可以参考使用(需先按照guide设置好BIOS)，**使用的时候请在CCG中换一个SMBIOS再使用**，否则会因为机器有同一个硬件ID而被苹果封锁。

## update log

#### 20190617：升级usb wifi网卡驱动
  - CF-915AC新版本的驱动都无法稳定支持5G，请使用`Apps/EW-7811Un_Mac_driver_v1.0.1.4.zip`
  - CF-811AC新版的驱动都可以用，更小更便宜，请使用`Apps/RTLWlanU_MacOS10.9_MacOS10.14_Driver_1830.20.b31_1827.4.b32_UI_5.0.8.b4.zip`，另[官方下载地址](http://www.comfast.cn/index.php?m=content&c=index&a=show&catid=30&id=335)

#### 20190610：升级clover，主题精简
  - 使用multibeast-11.3.0升级clover到r4934
  - 新增thinkpad e450/t450 Laptop的EFI，见t450分支
  - 主题仅保留一个最简的Minimalism主题

![](EFI/CLOVER/themes/Minimalism/screenshot.png)