# 黑苹果-Dell-Inspiron-7580

## 语言: 简体中文或[English](README_en.md)

## opencore 版本 0.7.1 点击右边的release下载最新的

## macOS 版本 11.4(Big Sur)

## 笔记本信息

|    cpu    |    i5-8265u     |
| :-------: | :-------------: |
|    gpu    |     uhd620      |
| 硬盘 | Kioxia Rd10 |
|   声卡   | realtak ALC 295 |
|  网卡  |     DW1820a (支持蓝牙耳机连接，用着挺舒服)     |

## Bios 设置 (有些dell笔记本没有的设置就别管它)

|               禁用                |
| :----------------------------------: |
|              Fast Boot               |
| CFG Lock (MSR 0xE2 write protection) 文章末尾教程。挺重要，能解锁最好，不能解锁要自己修改config几个设置 |
|                 VT-d                 |
|                 CSM                  |
|              Intel SGX               |

|         启用          |
| :---------------------: |
|          VT-x           |
|    Above 4G decoding    |
|     Hyper Threading     |
|   Execute Disable Bit   |
|   EHCI/XHCI Hand-off    |
| OS type: Windows 8.1/10 |
|    Legacy RTC Device    |

## 正常工作

* 核显
* 声卡
* hdmi (没试过)
* 所有的usb插槽和type-c  (type-c可以用来当充电孔，视频输出没试过)
* 有线网卡 
* wifi (原生网卡不可以，必须要换别的网卡才行，我换的是BCM94360Z3)
* 蓝牙 (原生网卡不可以，必须要换别的网卡才行，我换的是BCM94360Z3)
* 触控板
* 电量显示
* 摄像头
* cpu变频，gpu变频
* 音量快捷键和背光快捷键 (背光快捷键是这个：Fn + S(亮) Fn + B(暗) 如果要使用F11、F12要改acpi，我懒)

## 不正常工作
* mx150 (笔记本的英伟达显卡基本无法驱动)
* 睡眠 (这个东西有点复杂，本人电脑基本没怎么用这个功能，所以没管他) 

## 参考资料
* https://blog.daliansky.net/ 
* https://github.com/queensferryme/Hackintosh-Dell-7580
* https://github.com/daliansky/Hackintosh

## 怎样禁用CFG

1. 使用 bootx64.efi 启动你的电脑  (shell 压缩文件，https://github.com/ppjjhh/Hackintosh-Dell-Inspiron-7580/releases/tag/Shell)

2. 输入 **setup_var 0x5C3** 检查CFG是否已被禁用 PS:  *0x01*=启用, *0x00*=禁用

3. 输入 **setup_var 0x5C3 0x00** 禁用CFG

4. 再次输入 **setup_var 0x5C3** 看是否已被禁用(参考2).  PS: 看到这句话 **offset 0x5C3 is 0x00** 就说明你成功禁用掉CFG了

5. 输入 **exit** 退出此界面并重启


​     
