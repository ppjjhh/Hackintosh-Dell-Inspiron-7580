# 黑苹果-Dell-Inspiron-7580 （本人要考试，没时间，所以目前不再维护，非常抱歉）

## 语言: 简体中文或[English](README_en.md)

## opencore 版本 0.6.0

## macOS 版本 10.15.6

## 笔记本信息

|    cpu    |    i5-8265u     |
| :-------: | :-------------: |
|    gpu    |     uhd620      |
| 硬盘 | Hikvision C2000 |
|   声卡   | realtak ALC 295 |
|  网卡  |     DW1820a     |

## Bios 设置 (有些dell笔记本没有的设置就别管它)

|               禁用                |
| :----------------------------------: |
|              Fast Boot               |
| CFG Lock (MSR 0xE2 write protection) |
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
* hdmi (热插拔会自动重启，不知道怎么回事)
* 所有的usb插槽和type-c  (type-c可以用来当充电孔，视频输出没试过)
* 有线网卡 
* wifi (原生网卡不可以，必须要换别的网卡才行，我换的是1820a)
* 触控板
* 电量显示
* 摄像头
* cpu变频，gpu变频
* 音量快捷键和背光快捷键 (背光快捷键是这个：Fn + S 或者 Fn + B，F11、F12的要改acpi，我懒)

## 不正常工作
* mx150 (笔记本的英伟达显卡基本无法驱动)
* 睡眠 (这个东西有点复杂，本人电脑基本没怎么用这个功能，所以没管他) 
* 这个acpi文件是我自己电脑的原生acpi，有些电脑可能用不了，你可以提取自己的试试

## 参考资料
* https://blog.daliansky.net/ 
* https://github.com/daliansky/Hackintosh

## 怎样禁用CFG

1. 使用 bootx64.efi 启动你的电脑  (shell 压缩文件)

2. 输入 **setup_var 0x5C3** 检查CFG是否已被禁用 PS:  *0x01*=启用, *0x00*=禁用

3. 输入 **setup_var 0x5C3 0x00** 禁用CFG

4. 再次输入 **setup_var 0x5C3** 看是否已被禁用(参考2).  PS: 看到这句话 **offset 0x5C3 is 0x00** 就说明你成功禁用掉CFG了

5. 输入 **exit** 退出此界面并重启

## 下面的图片是关于禁用CFG的，如果加载不出来，多刷新几次就好了


   ![Folder hierarchy](https://github.com/ppjjhh/Hackintosh-Dell-Inspiron-7580/blob/master/image/ScreenShot.jpeg)

   ![Step 1](https://github.com/ppjjhh/Hackintosh-Dell-Inspiron-7580/blob/master/image/1.jpeg)

   ![Step 2](https://github.com/ppjjhh/Hackintosh-Dell-Inspiron-7580/blob/master/image/2.jpeg)

   ![Step 3](https://github.com/ppjjhh/Hackintosh-Dell-Inspiron-7580/blob/master/image/3.jpeg)

   ![Step 4](https://github.com/ppjjhh/Hackintosh-Dell-Inspiron-7580/blob/master/image/4.jpeg)

   ![Step 5](https://github.com/ppjjhh/Hackintosh-Dell-Inspiron-7580/blob/master/image/5.jpeg)

   ![Step 6](https://github.com/ppjjhh/Hackintosh-Dell-Inspiron-7580/blob/master/image/6.jpeg)

   ![Step 7](https://github.com/ppjjhh/Hackintosh-Dell-Inspiron-7580/blob/master/image/7.jpeg)

   ![Step 8](https://github.com/ppjjhh/Hackintosh-Dell-Inspiron-7580/blob/master/image/8.jpeg)

   ![Step 9](https://github.com/ppjjhh/Hackintosh-Dell-Inspiron-7580/blob/master/image/9.jpeg)

   ![Step 10](https://github.com/ppjjhh/Hackintosh-Dell-Inspiron-7580/blob/master/image/10.jpeg)

   ![Step 11](https://github.com/ppjjhh/Hackintosh-Dell-Inspiron-7580/blob/master/image/11.jpeg)

   ![Step 12](https://github.com/ppjjhh/Hackintosh-Dell-Inspiron-7580/blob/master/image/12.jpeg)

   ![Step 13](https://github.com/ppjjhh/Hackintosh-Dell-Inspiron-7580/blob/master/image/13.jpeg)

   
