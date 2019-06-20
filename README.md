
[![996.icu](https://img.shields.io/badge/link-996.icu-red.svg)](https://996.icu)
[![LICENSE](https://img.shields.io/badge/license-Anti%20996-blue.svg)](https://github.com/996icu/996.ICU/blob/master/LICENSE)

这是一个我个人使用、持续更新维护的构建列表，每一种构建点击进去可以查看详情。

### 已有Build：
- iMac 4K 2019:

![](./msi_b360m_i3_8100_rx570_imac_4k_2019/imac_info_neofetch.png)
- Macmini 2018:
待更新
- MBP13 2015:
待更新
- 以前用的老平台
  - 完全免驱动，未记录EFI，tonymac的工具直接驱动，无需做任何修改和驱动处理。捡垃圾的话，十分便宜，估计1k，日常使用无忧。
    - intel core i3-3220
    - Asus B75M-A
    - Kingston DDR3-1600 4G*2
    - 七彩虹 GTX 650Ti
    - WD 1T, 5400rpm HDD(其实系统加载完以后真的不算卡比起老版的imac)
  - 同理还可以用e3 1230等便宜量足的U提升性价比。

### 辅助工具
- mac_utils: 提供一些驱动、硬件检测应用等工具。
- neofetch: 查看系统spec
- 查看cpu核心数: `sysctl hw.physicalcpu`, `sysctl hw.logicalcpu`
- 查看空余内存: `alias free="top -l 1 -s 0 | grep PhysMem"`
