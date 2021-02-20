## iMac (Retina 5K, 27-inch, 2019) Hackintosh

| Item | Spec |
|:------|:------|
|系统   | macOS 10.15.7 Catalina |
|处理器 | Intel® Core™ i5-8400 |
|主板   | Asus Prime B360M-A |
|内存   | G.Skill DDR4 8G * 2 |
|硬盘   | Intel® SSD 760p Series (256GB, M.2 80mm, PCIe* 3.0 x4, 3D2, TLC) |
|显卡   | Yeston RX 570 GAMEACE (4GB GDDR5, 256 bit, 2048 CORES |
|网卡   | Realtek Ethernet RTL8111H + CF-811AC USB WiFi |
|声卡   | Realtek® ALC887 Codec |
|Clover版本| r5100 |


## Releases Log

#### 20210220:
- EFI基本稳定，不再做更新。

#### 20201111: 升级10.15.7和补充更新
- 升级补充更新后，不能关机，强制关机后音量丢失；进入windows后重新进macos系统解决。

#### 202009: 升级10.15.6

#### 20200527: 升级10.15.5

#### 20200326: 升级10.15.4

#### 20200302: 升级10.15.3
- 更新kexts，平滑升级系统。

#### 20200102：稳定构建
- 启动、关机问题：
  - (1) 删除AptioMemoryFix-64.efi，添加OsxAptioFix2Drv-free2000.efi 和 EmuVariableUefi-64.efi；同时修改config.plist的boot模块添加slide=0。解决安装卡最后2分钟的问题。
  - (2) Acpi->Fixes勾选FixShutDown，解决关不了机问题。