# DELL7472 OpenCore配置文件（也可供7572机型参考）

## 使用环境
* Windows11

* macOS13.0 beta

* 一个512M FAT32分区用来存放EFI文件夹，ESP分区单独留给Win11使用，维护OC无需挂载ESP分区

## BIOS设置

* 关闭『安全引导』

* 开启AHCI

* 关闭『Enable Legacy Option ROMs』

## 特别注意

* Msr请自行解锁，如果不想解锁，可在配置文件里面勾选“AppleXcpmCfgLock”，否则引导过程中会卡住

* 如果需要安装Windows11，请在BIOS安全设置里面开启“PTT”

* 设置任何HiDPI分辨率的工具和方法在此：https://github.com/usr-sse2/RDM

* 关于机型的选择，个人推荐“MacBookAir8,2”，这个选择从CPU的频率策略上来说，算是非常平衡的，当然选择其他机型也是能正常运转的，可根据自己的喜好进行合理选择

## 机器配置

* BIOS版本：1.3.1（建议大家及时更新BIOS）

* CPU：i5-8250U

* 声卡：ALC256，声卡ID使用69（十进制），驱动文件名称为ALC256.kext，目前已非常完善，最新版可在此下载：https://github.com/ic005k/ALC256

* 内存：8G

* 核显：UHD620（无独显）

* 独显：无

* 硬盘：256G SSD

* 无线网卡：BCM94360CS2（后来更换，免驱，EFI里面不存在任何无线网卡驱动）

## 目前存在的问题

* HDMI输出测试正常，但不一定广泛适应，也可能会存在不可知的兼容性问题，欢迎大家反馈问题

## 最后对所有的贡献者和参与者一并表示感谢！
