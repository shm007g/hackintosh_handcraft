## iMac (Retina 4K, 21.5-inch, 2019) Hackintosh

| Item | Spec |
|------|------|
|系统   | macOS 10.15.1 Catalina |
|处理器 | Intel i5-4670T (4) @ 2.30GHz |
|主板   | Dell OptiPlex 9020m |
|内存   | Samsung 4G*2 DDR3L-1600MHz |
|硬盘   | Samsung 256G 850 EVO |
|显卡   | Intel HD Graphics 4600 |
|网卡   | DW1820a(CN-08PKF4) |
|声卡   | Realtek® ALC3234 Codec |
|Clover版本| r5099 |

现状：目前声卡、网卡、硬解、睡眠、HWMonitor温度检测均正常。


视觉参考：
![](https://static.chiphell.com/forum/201911/13/164831zex3mbkz96wmkj3k.jpg)

## Releases Log

#### 20191208: fix airdrop 中文不能用问题
  - add AirportBrcmFixup.kext and country auto-detect

#### 20191128: fix USB 3.0接口需要供电的问题
  - 接口已经定制，去掉USBInjectAll.kext

#### 20191123: 构建
  - 最新的Clover和kexts驱动，基本功能OK。