## 2018 Mac Mini Hackintosh

| Item | Spec |
|:------|:------|
|系统   | macOS 10.15.3 |
|处理器 | Intel Core i3-8100 @ 3.6GHz |
|主板   | Onda H310SD3-ITX |
|内存   | Onda 8G*2 DDR3 1600MHz |
|硬盘   | Intel 540s 360G M.2 Sata |
|显卡   | Intel UHD Graphics 630 |
|网卡   | CF-811AC USB WIFI |
|Clover| r5100 |

### 硬件：
- CPU：2018年发布的Intel 8代core i3，性能得到了相当的提升。4核@3.6GHz的i3-8100，日常办公影音空闲率在50%以上，性能上够用，TDP 65W散热基本问题不大。
- 显卡：i3自带的UHD630的性能也还可以，普通带一两个1080P显示器问题也不大。
- 主板+存储：Mini主机压缩预算考虑，选了昂达全固态H310ITX板子，选用DDR3专用条，可以省下一笔钱，使用了Intel 540S M.2 Sata SSD。
- 机箱+电源：Mini主机选用了外置电源DC-ATX适配器+联达直插式电源的方式，静音；机箱选用了4mm铝合金机箱，大小`19*19*6,5`，只需要30块的大镰刀下压风扇，基本上散热静音都OK了。这款小主机配置和Mac Mini2018基础款差不多，618不到¥1800就拿下了，很划算，已稳定办公半年左右。

![](./L65_itx_case.png)


## Releases Log

#### 20200316: 平滑升级catalina 10.15.3
  - kexts版本到最新，重启进入“Boot Macos Install From Data” 平滑升级catalina

#### 20191231: 升级catalina
  - 升级clover和kexts版本到最新，重启三次进入“Boot Macos Install From***” 平滑升级catalina

#### 20190620：稳定构建
  - 在tonymac tools安装和驱动安装完毕后，基于pcbeta某大神在config.plist中设定的dsdt patch，完成构建。