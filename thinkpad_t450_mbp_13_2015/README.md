## MacBook Pro (Retina, 13-inch, Early 2015) Hackintosh

| Item | Spec |
|:------|:------|
|系统   | macOS 10.14.6 + Windows 10 |
|Laptop| ThinkPad T450 |
|处理器 | Intel Core i5-5300u @ 2.3GHz |
|内存   | 8G*2 DDR3-1600MHz |
|硬盘   | BIWIN msata 256G + 500G HDD |
|显卡   | Intel HD Graphics 5500 1536 MB|
|网卡   | CF-811AC USB WIFI |
|声卡   | Realtek® ALC3232 Codec |
|Clover| r5099 |

问题：耳机孔爆音，外接vga无法使用。

## Releases Log

#### 20190824：升级到10.14.6
  - 升级了3个kext驱动，直接系统更新到10.14.6


#### 20191130
  - 升级Clover到最近，USB Limit解除

#### 20190610：升级clover，主题精简
  - 使用multibeast-11.3.0升级clover到r4934
  - 新增thinkpad e450/t450 Laptop的EFI，见t450分支
  - 主题仅保留一个最简的Minimalism主题

![](EFI/CLOVER/themes/Minimalism/screenshot.png)
