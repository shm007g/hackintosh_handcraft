## iMac (Retina 5K, 27-inch, 2019) Hackintosh

| Item | Spec |
|:------|:------|
|系统   | macOS 10.15.3 Catalina |
|处理器 | Intel Core i5-8400 @ 2.8GHz |
|主板   | Asus Prime B360M-A |
|内存   | G.Skill 8G * 2 DDR4 |
|硬盘   | Intel 760P M.2 NVMe SSD + 1T HDD |
|显卡   | Yeston Radeon RX570 4G GDDR5|
|网卡   | 板载 Realtek RTL8111H + CF-811AC USB WiFi |
|声卡   | Realtek® ALC887 Codec |
|Clover版本| r5100 |


## Releases Log

#### 20200302: 升级10.15.3
- 更新kexts，平滑升级系统。

#### 20200102：稳定构建
- 启动、关机问题：（1）删除AptioMemoryFix-64.efi，添加OsxAptioFix2Drv-free2000.efi 和 EmuVariableUefi-64.efi；同时修改config.plist的boot模块添加slide=0。解决安装卡最后2分钟的问题。（2）Acpi->Fixes勾选FixShutDown，解决关不了机问题。