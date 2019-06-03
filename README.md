
[![996.icu](https://img.shields.io/badge/link-996.icu-red.svg)](https://996.icu)
[![LICENSE](https://img.shields.io/badge/license-Anti%20996-blue.svg)](https://github.com/996icu/996.ICU/blob/master/LICENSE)


## update

#### 20190529：新增themes

#### 20190519：新增硬件检测
  - 新增Applications文件夹，存放硬件检测软件
  - 新增HWMonitor和相关的kexts，主要是为了看温度
  - 新增VideoProc查看硬件解码(当然是都ok啦)
  - CPU-S, intel(R) Power Gadge查看系统cpu变频之类的

#### 20190519：升级到mojave10.14.5
  - Clover版本过低可能引发错误：因为我最近使用了最新的Multibeast做的Clover引导，版本4920很新；
  - kexts版本过低可能引发错误：从CCG里面看kexts也都很新；
  - 系统更新报错(An error occurred while installing the selected updates)：下载macos combo更新来安装；升级过程开启了-v查看细节，基本无人值守可以自行安装完成；
  - 更新细节：更新中会有一个新的 `Install MAC` clover boot选项，更新中会自动进入这个2次吧，最后这个选项消失，更新就完成了；然后CLover boot选项会变得和之前一样。

#### 20190517：修复无法预览jpg图片错误
预览要集成显卡的硬解功能
  - 我的i3-8100有集成显卡的，于是在bios里面开启igpu就可以了。
  - 网上的教程是把smbios改成不带集成显卡的机器，然后用NoVPAJpeg.kext来fix。

#### 20190517：修复shutdown reboots(关机重启)错误
  - BIOS降级: 请使用7B53v14或者13版本的bios，再高会出现问题。
  - 进入/EFI/CLOVER/drivers64UEFI；删除AptioMemoryFix-64.efi，添加OsxAptioFix2Drv-free2000.efi 和 EmuVariableUefi-64.efi；同时修改config.plist的boot模块添加slide=0。

## My Hackintosh Build
- 基于tonymac网站的 install guide，使用unibeast和multibeast安装；
- hackintosh对新的8代9代intel芯片组支持度很好，没有什么大的问题。
- 我的用途是办公和日常使用，不纠结具体的facetime之类的，icloud正常就行了。
- 我的硬件如下(换个i5-8500打败iMac2019的基本款配置😂，价格大概是1/5~1/4左右)：

|hardware|spec|
|-|-|
|CPU |Intel i3-8100|
|主板|MSI B360m Fire|
|显卡|盈通 RX570 4g|
|内存| 海盗船 DDR4-2400 8G * 2|
|硬盘|Intel 760p 256g nvme ssd|
|机械硬盘|西数蓝盘1T(7200RPM,65M缓存)|
|无线网络|Comfast CF-915AC 双频 USB WIFI|
|系统|MacOS 10.14.2|
|BIOS|7B53v14|

**注意**：
1. multibeast原生会把kext安装到/L/E下面，为了保持kexts的稳定性，我建议把所有驱动搬迁到/EFI/CLOVER/Kexts/$(version)下面去;
2. 调整kexts后最好重建下kext缓存，以免开机起不来之类的；操作指令`sudo kextcache -i /`。网上有很多用Kext Utility操作的，我看日志应该和kextcache操作原理差不多。

## Last Build
下面是上一套我用来hackintosh的老硬件，完全免驱，tonymac的工具直接驱动，无需做任何修改和驱动处理。捡垃圾的话，十分便宜，估计1k，日常使用无忧。

- intel core i3-3220
- Asus B75M-A
- Kingston DDR3-1600 4G*2
- 七彩虹 GTX 650Ti
- WD 1T, 5400rpm HDD(其实系统加载完以后真的不算卡比起老版的imac)

## macos spec
- neofetch: 查看系统spec
- 查看cpu核心数:`sysctl hw.physicalcpu`, `sysctl hw.logicalcpu`
- 查看空余内存: `alias free="top -l 1 -s 0 | grep PhysMem"`
