## iMac (Retina 4K, 21.5-inch, 2019) Hackintosh

| Item | Spec |
|:------|:------|
|系统   | macOS 10.15.2 Catalina |
|型号   | Dell OptiPlex 9020m |
|处理器 | Intel i5-4670T (4) @ 2.30GHz |
|内存   | Samsung 4G*2 DDR3L-1600MHz |
|硬盘   | Samsung 256G 850 EVO |
|显卡   | Intel HD Graphics 4600 |
|网卡   | DW1820a(CN-08PKF4) |
|声卡   | Realtek® ALC3234 Codec |
|Clover版本| r5099 |

### 硬件:
- 4代U现在已经进入了性价比非常高的阶段，4核4线程的i5，价格三四百。Dell 9020M/HP 800G1 DM这样的4代顶级Q87芯片组小机箱，仅·`18*18*3.5`和一本书差不多大，准系统也才三四百，都买不到上面一块昂达的ITX，Dell/HP做工应该还是蛮不错。CPU选择i5-4670T，Benchamrk数据比i5-6500T要好，i5-6500T需要搭乘的7040M准系统也更加贵😝。
- 咸鱼到手后，全部拆了一遍，清灰上了Arctic的硅脂，这几天稳定下来后，温度维持在30～50度之间。CPU风扇声音有点嗡嗡嗡蚊子叫，有机会换新的风扇。

![](https://static.chiphell.com/forum/201911/13/164831zex3mbkz96wmkj3k.jpg)

## Releases Log

#### 20200102: 不再支持
  - EFI已经稳定，请自行更行CLOVER和KEXTS升级MacOS。  
  - 下载地址：https://github.com/shm007g/hackintosh_handcraft/releases/tag/20200102

#### 20191208: fix airdrop 中文不能用问题
  - add AirportBrcmFixup.kext and country auto-detect

#### 20191128: fix USB 3.0接口需要供电的问题
  - 接口已经定制，去掉USBInjectAll.kext

#### 20191123: 构建
  - 最新的Clover和kexts驱动，基本功能OK。
