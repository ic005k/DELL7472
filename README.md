# DELL7472 OpenCore配置文件及驱动（也可供7572机型参考，二者主要存在屏幕大小的区别）

本配置完全基于OpenCore，Clover上已不再测试和维护，请大家知悉。我目前的使用环境是：Windows11 + MacOS12.0beta。

特别注意：安装使用黑苹果之前，需要在BIOS里面进行如下设置，3项设置缺一不可，都是必须要设置的，否则将会导致引导出现问题：

1.关闭『安全引导』

2.开启AHCI

3.关闭『Enable Legacy Option ROMs』

目前完全支持12.0且兼容11.0等系统，功能及驱动等等一切正常。

如果需要安装Windows11，请在BIOS安全设置里面开启“PTT”。

具体文件请到发行页面下载：https://github.com/ic005k/DELL7472/releases



机器配置如下：

BIOS版本：1.3.1（建议大家及时更新BIOS）

CPU：i5-8250U

声卡：ALC256，声卡ID使用69（十进制），驱动文件名称为ALC256.kext，目前已非常完善

内存：8G

核显：UHD620

独显：无（同时显卡的设备属性里面已添加屏蔽独显的代码）

硬盘：256G SSD

无线网卡：BCM94360CS2（后来更换，免驱）



特别注意：

0.连接HDMI开机，如果笔记本内屏一直出现黑屏现象，则建议开启HiDPI看看，这个现象和没有开启HiDPI有非常直接的关系。

1.我使用的是苹果原装网卡BCM94360CS2，所以驱动里面没有放任何无线网卡和蓝牙的驱动程序，大家自行根据自己的无线网卡型号放入相应的驱动。

目前存在的问题：

1.如果在插上耳机的情况下进入Recovery，此时选择『重启系统』，会导致机器直接关机。需拔下耳机并关掉交流电源（如果连接有电源适配器），等待5分钟左右，才可以正常开机。目前此问题无解。
所以，如果进行OTA升级或安装新系统，建议拔掉耳机再进行。

20210908注：目前已经解决了这个问题，感谢 @szhifei ！详情：https://github.com/ic005k/DELL7472/issues/47

2.MacOS11.0环境下，如果通过HDMI连接外屏，在没有睡眠唤醒的情况下，如果拔掉HDMI，则内屏会一直黑屏。在这之前，如果有睡眠唤醒的过程，则无此现象。

最后对所有的贡献者和参与者一并表示感谢！
