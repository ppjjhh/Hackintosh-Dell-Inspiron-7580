# Hackintosh-Dell-Inspiron-7580(Sorry, This repository will no longer maintained.)

## Language: English or [简体中文](README.md)

## opencore version 0.6.4

## macOS version 10.15.6

## Computer Info

|    cpu    |         i5-8265u         |
| :-------: | :----------------------: |
|    gpu    |          uhd620          |
| Hard disk |       Kioxia Rd10        |
|   audio   |     realtak ALC 295      |
|  network  | DW1820a(AirPods support) |

## Bios setting (Ignore it if your bios don't have these item)

|               Disable                |
| :----------------------------------: |
|              Fast Boot               |
| CFG Lock (MSR 0xE2 write protection) |
|                 VT-d                 |
|                 CSM                  |
|              Intel SGX               |

|         Enable          |
| :---------------------: |
|          VT-x           |
|    Above 4G decoding    |
|     Hyper Threading     |
|   Execute Disable Bit   |
|   EHCI/XHCI Hand-off    |
| OS type: Windows 8.1/10 |
|    Legacy RTC Device    |

## work

* uhd620
* audio
* hdmi (untested)
* All usb and type-c (you can use this slot to charge your computer)
* network (Wired network)
* wifi (you must change the native wireless network adapter)
* Trackpad
* battery and power display
* camera
* cpu frequency & power & temperature & utilization
* volume and backlight shortcut (Fn + S or Fn + B)

## not work
* mx150 (blame nvidia)
* Sleep (so complex that i have no time to fix it. :) 
* the acpi file is my computer's native file, so some computer may not work well. 

## Reference
* https://blog.daliansky.net/
* https://github.com/daliansky/Hackintosh

## How to Unlock CFG

1. Use the bootx64.efi to boot your computer.

2. Type in **setup_var 0x5C3** to check the CFGLock status.   PS:  *0x01*=lock, *0x00*=unlock

3. Type in **setup_var 0x5C3 0x00** to unlock the CFGLock.

4. Type in **setup_var 0x5C3** again to confirm if it is succeed.  PS: It means you are succeed when the screen shows this sentence:  **offset 0x5C3 is 0x00**.

5. Type in **exit** to restart your computer. 

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
   
   
