
[![996.icu](https://img.shields.io/badge/link-996.icu-red.svg)](https://996.icu)
[![LICENSE](https://img.shields.io/badge/license-Anti%20996-blue.svg)](https://github.com/996icu/996.ICU/blob/master/LICENSE)

这是一个我个人使用、持续更新维护的构建列表，每一种构建点击进去可以查看详情。

## 已有Build：
### iMac 4K 2019:

![](./msi_b360m_i3_8100_rx570_imac_4k_2019/imac_4k_2019_info.png)

### Macmini 2018:

```
                    'c.          shm@macmini.local 
                 ,xNMM.          ----------------- 
               .OMMMMo           OS: macOS Mojave 10.14.4 18E226 x86_64 
               OMMM0,            Host: Hackintosh (SMBIOS: Macmini8,1) 
     .;loddo:' loolloddol;.      Kernel: 18.5.0 
   cKMMMMMMMMMMNWMMMMMMMMMM0:    Uptime: 28 mins 
 .KMMMMMMMMMMMMMMMMMMMMMMMWd.    Packages: 36 (brew) 
 XMMMMMMMMMMMMMMMMMMMMMMMX.      Shell: bash 3.2.57 
;MMMMMMMMMMMMMMMMMMMMMMMM:       Resolution: 2560x1080 
:MMMMMMMMMMMMMMMMMMMMMMMM:       DE: Aqua 
.MMMMMMMMMMMMMMMMMMMMMMMMX.      WM: Quartz Compositor 
 kMMMMMMMMMMMMMMMMMMMMMMMMWd.    WM Theme: Blue (Light) 
 .XMMMMMMMMMMMMMMMMMMMMMMMMMMk   Terminal: Apple_Terminal 
  .XMMMMMMMMMMMMMMMMMMMMMMMMK.   Terminal Font: SFMono-Regular 
    kMMMMMMMMMMMMMMMMMMMMMMd     CPU: Intel i3-8100 (4) @ 3.60GHz 
     ;KMMMMMMMWXXWMMMMMMMk.      GPU: Intel UHD Graphics 630 
       .cooc,.    .,coo:.        Memory: 5164MiB / 16384MiB 

                                                         
```

### MBP13 2015:

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

### 以前用的老平台
  - 完全免驱动，未记录EFI，tonymac的工具直接驱动，无需做任何修改和驱动处理。捡垃圾的话，十分便宜，估计1k，日常使用无忧。
    - intel core i3-3220
    - Asus B75M-A
    - Kingston DDR3-1600 4G*2
    - 七彩虹 GTX 650Ti
    - WD 1T, 5400rpm HDD(其实系统加载完以后真的不算卡比起老版的imac)
  - 同理还可以用e3 1230等便宜量足的U提升性价比。

## 辅助工具
- mac_utils: 提供一些驱动、硬件检测应用等工具。
- neofetch: 查看系统spec
- 查看cpu核心数: `sysctl hw.physicalcpu`, `sysctl hw.logicalcpu`
- 查看空余内存: `alias free="top -l 1 -s 0 | grep PhysMem"`
