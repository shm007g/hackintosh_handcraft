
[![996.icu](https://img.shields.io/badge/link-996.icu-red.svg)](https://996.icu)
[![LICENSE](https://img.shields.io/badge/license-Anti%20996-blue.svg)](https://github.com/996icu/996.ICU/blob/master/LICENSE)

这是一个我个人使用、维护的Hackintosh构建列表，选择的都是便宜的办公硬件，点击相应的文件夹进去可以查看详情。

## 列表一览：
### iMac 4K 2019:
```
                    'c.          szymon@iMac.local
                 ,xNMM.          -----------------
               .OMMMMo           OS: macOS Mojave 10.14.6 18G87 x86_64
               OMMM0,            Host: Hackintosh (SMBIOS: iMac19,2)
     .;loddo:' loolloddol;.      Kernel: 18.7.0
   cKMMMMMMMMMMNWMMMMMMMMMM0:    Uptime: 4 mins
 .KMMMMMMMMMMMMMMMMMMMMMMMWd.    Packages: 44 (brew)
 XMMMMMMMMMMMMMMMMMMMMMMMX.      Shell: bash 3.2.57
;MMMMMMMMMMMMMMMMMMMMMMMM:       Resolution: 2560x1080@2x
:MMMMMMMMMMMMMMMMMMMMMMMM:       DE: Aqua
.MMMMMMMMMMMMMMMMMMMMMMMMX.      WM: Quartz Compositor
 kMMMMMMMMMMMMMMMMMMMMMMMMWd.    WM Theme: Blue (Light)
 .XMMMMMMMMMMMMMMMMMMMMMMMMMMk   Terminal: iTerm2
  .XMMMMMMMMMMMMMMMMMMMMMMMMK.   Terminal Font: Monaco 12
    kMMMMMMMMMMMMMMMMMMMMMMd     CPU: Intel i3-8100 (4) @ 3.60GHz
     ;KMMMMMMMWXXWMMMMMMMk.      GPU: Radeon RX 570
       .cooc,.    .,coo:.        Memory: 5203MiB / 16384MiB
```

### Macmini 2018:
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

### MBP13 2015:
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

### 一套tonymac工具直接免驱的老平台
    - intel core i3-3220
    - Asus B75M-A
    - Kingston DDR3-1600 4G*2
    - 七彩虹 GTX 650Ti
    - WD 1T, 5400rpm HDD(其实系统加载完以后真的不算卡比起老版的imac)
  - 同理还可以用e3 1230等便宜量足的U提升性价比。

## 辅助工具
- mac_utils: 提供一些驱动、硬件检测应用、软件激活工具，不是系统构建的必需品。
- neofetch: 查看系统spec
- 查看cpu核心数: `sysctl hw.physicalcpu`, `sysctl hw.logicalcpu`
- 查看空余内存: `alias free="top -l 1 -s 0 | grep PhysMem"`
