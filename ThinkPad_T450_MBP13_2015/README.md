## MacBook Pro (Retina, 13-inch, Early 2015) Hackintosh

| Item | Spec |
|:------|:------|
|系统   | macOS 10.15.3 + Windows 10 |
|Laptop| ThinkPad T450 |
|处理器 | Intel Core i5-5300u @ 2.3GHz |
|内存   | 8G*2 DDR3-1600MHz |
|硬盘   | BIWIN msata 256G + 500G HDD |
|显卡   | Intel HD Graphics 5500 1536 MB|
|网卡   | CF-811AC USB WIFI |
|声卡   | Realtek® ALC3232 Codec |
|Clover| r5097 |


## Releases Log

## 20200530: 不再支持
  - EFI在10.15.3系统下还算比较稳定。迫于机器被收回，无法支持了。EFI下载地址：https://github.com/shm007g/hackintosh_handcraft/releases/tag/20200320 

## 20200320: fix耳机孔爆音，睡眠
  - 爆音：使用EFI/alc_fix/install.sh安装，把/bin/ALCPlugFix加入到启动项，这样每次启动都能修复
  - 睡眠通过添加kext fix

## 20200319: 重新整理升级到10.15.3
  - 感谢jsassu20提供的[EFI](https://github.com/jsassu20/Lenovo-ThinkPad-T450-macOS-Catalina)，除了睡眠、耳机爆音无法正常外，所有均正常，minidp据说可以输出，vga不行。

#### 20190824：升级到10.14.6
  - 升级了3个kext驱动，直接系统更新到10.14.6
  - 使用alc_fix下面的install.sh解决耳机爆音的问题

#### 20191130
  - 升级Clover到最近，USB Limit解除

#### 20190610：升级clover，主题精简
  - 使用multibeast-11.3.0升级clover到r4934
  - 新增thinkpad e450/t450 Laptop的EFI，见t450分支
  - 主题仅保留一个最简的Minimalism主题

![](EFI/CLOVER/themes/Minimalism/screenshot.png)
