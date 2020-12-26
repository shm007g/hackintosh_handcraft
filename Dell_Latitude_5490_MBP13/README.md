## MacBook Pro (13-inch, 2018, Four Thunderbolt 3 Ports) Hackintosh

| Item | Spec |
|:------|:------|
|系统   | macOS 10.15.4 Catalina |
|型号   | [Dell Latitude 5490 Laptop](https://dl.dell.com/topicspdf/latitude-14-5490-laptop_owners-manual_zh-cn.pdf) |
|处理器 | Intel® Core™ i5-8250U |
|内存   | SK Hynix DDR4 8G * 2 |
|硬盘   | SK hynix SC311 SATA 256GB|
|显卡   | Intel UHD Graphics 620 |
|网卡   | Intel® Ethernet I219-LM + Intel® Dual Band Wireless-AC 8265 |
|外置网卡| CF-811AC USB WiFi |
|声卡   | Realtek® ALC3246 Codec |
|Clover版本| r5119 |


## Releases Log

#### 20201226: 基本装机完成
- 安装系统：参考[tonymacx86的install guide](https://www.tonymacx86.com/threads/unibeast-install-macos-catalina-on-any-supported-intel-based-pc.285366/)；下载catalina 10.15.4 dmg镜像，安装成Applications；F12配置笔记本BIOS；使用Unibeast 10.3.0制作安装U盘。安装U盘引导出问题，搜索得到[解决办法](https://www.tonymacx86.com/threads/catalina-cant-reach-installer.306933/page-2)；格式化硬盘为AppleFS进行安装，安装完成。第一次进入系统需要无线键盘和鼠标配置macOS系统。用Clover Configurator从U盘里面把EFI拷贝到系统盘的ESP目录，进入Windows使用EasyUEFI新增加一个MacOS引导项，添加`EFI/BOOT/BOOTX64.efi`文件；重新启动电脑从MacOS引导进入。
- 安装驱动：
  - （1）使用MultiBeast 12.3.0进行通用驱动的安装；使用Hackintools-内核扩展补气最新的通用驱动：IntelMausi网卡驱动，WEG驱动，USBInjectAll驱动，VirtualSMC系列驱动尤其SMCBatteryManager.kext，效能提升安装CPUFriend.kext和NoTouchID.kext，Intel蓝牙驱动IntelBluetoothFirmware.kext和IntelBluetoothInjector.kext。
  - （2）键盘触摸板驱动：VoodooPS2Controller.kext和VoodooI2C开头的2个驱动，需要配合config文件。我试了几次触摸板一直不能用，就直接借鉴了[eduardoborges
/
latitude-5490-hackintosh](https://github.com/eduardoborges/latitude-5490-hackintosh)的config.plist, ACPI/patched, kexts 文件夹。
  - （3）参考[Sukka](https://blog.skk.moe/post/hackintosh-fix-magenta-screen/)使用Hackintool修复外接屏幕紫屏的问题。
- 待改善的地方：
  - 笔记本屏幕亮度调节没搞好；关闭盖子，不像白苹果那样关闭内屏，内容全部转到外屏上。
  - 音频带有线耳机听歌，人声有杂音，器乐OK，蓝牙耳机OK。eduardoborges的声卡配置的是ALC256可能和我的机器不太相符，要微调。