# Acer-Nitro-5-hackintosh
适用于Acer Nitro 5 AN515-52 (N17C1)的Hackintosh，Clover

请务必确认设备型号为Acer Nitro 5 AN515-52 (N17C1)，其它相似型号请按照实际配置自行确认

![image](https://github.com/JackyZHZ/Acer-Nitro-5-hackintosh/blob/master/screenshots/AN515-52.jpg)


配置
CPU：Intel i5-8300H
内存：8G*2
硬盘：Acer VT500M 256G（注意：三星PM981无法用于黑苹果）
核显：UHD630
独显：GTX 1650 4G
网卡：DW1560（也可用于DW1820A）
BIOS版本：V1.28

BIOS中需要注意的设置：
1. Main页面
    > Network Boot = Disabled (理论上缩短开机时间)
    > F12 Boot Menu = Enabled
    > SATA Mode = AHCI
    > Wake on LAN = Disabled
    > Touchpad = Advanced (已对触摸板进行热补丁，选择该模式可几乎完美实现苹果手势)
    > Function key behavior = Function Key (已对键盘进行热补丁，选择该模式配合"FN"键可实现键盘上部分快捷方式)
    > Lid Open Resume = Disabled
    > Wake on USB while lid closed = Disabled
    > D2D Recovery = Disabled
    > xHCI Support = Enabled
    > Keyboard Lighting Timeout = Enabled 
    > Fast Boot = Enabled
2. Advanced页面
    > Intel VTX = Enabled
    > Intel VTD = Enabled
    其它保持默认
3. Boot页面
    > Boot Mode = UEFI
    > Secure Boot = Disabled

目前实现情况：
1. 核显完美，由于目前无法驱动独显已进行屏蔽，降低整机功耗
2. 键盘及触摸板几乎完美，键盘大部分快捷功能都可使用（如音量控制），触摸板几乎完美实现苹果原生手势操作
3. Wifi、蓝牙可用隔空及接力
4. 完美休眠
目前发现不足：
1. 休眠唤醒后偶发性蓝牙不可用，蓝牙连接耳机等设备有时无法成功，目前暂未进行排查
2. 键盘灯无法控制，原因上硬件没有可用于调节的接口功能
