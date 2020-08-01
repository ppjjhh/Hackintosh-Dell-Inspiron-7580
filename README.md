# Hackintosh-Dell-Inspiron-7580

## opencore version 0.5.9

## macOS version 10.15.6

## Computer Info

|    cpu    |    i5-8265u     |
| :-------: | :-------------: |
|    gpu    |     uhd620      |
| Hard disk | Hikvision C2000 |
|   audio   | realtak ALC 295 |
|  network  |     DW1820a     |

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
* hdmi (sometime it will cause restart when you Hot Swap)
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

   ![Screen Shot 2020-07-31 at 21.33.56](https://github.com/ppjjhh/Hackintosh-Dell-Inspiron-7580/image/Screen Shot 2020-07-31 at 21.33.56.png)

   ![IMG_20200731_213606](/Volumes/Data/GithubRepo/EFI/Hackintosh-Dell-Inspiron-7580/image/IMG_20200731_213606.jpg)

   ![IMG_20200731_213617](/Volumes/Data/GithubRepo/EFI/Hackintosh-Dell-Inspiron-7580/image/IMG_20200731_213617.jpg)

   ![IMG_20200731_213627](/Volumes/Data/GithubRepo/EFI/Hackintosh-Dell-Inspiron-7580/image/IMG_20200731_213627.jpg)

   ![IMG_20200731_213705](/Volumes/Data/GithubRepo/EFI/Hackintosh-Dell-Inspiron-7580/image/IMG_20200731_213705.jpg)

   ![IMG_20200731_213711](/Volumes/Data/GithubRepo/EFI/Hackintosh-Dell-Inspiron-7580/image/IMG_20200731_213711.jpg)

   ![IMG_20200731_213733](/Volumes/Data/GithubRepo/EFI/Hackintosh-Dell-Inspiron-7580/image/IMG_20200731_213733.jpg)

   ![IMG_20200731_213744](/Volumes/Data/GithubRepo/EFI/Hackintosh-Dell-Inspiron-7580/image/IMG_20200731_213744.jpg)

   ![IMG_20200731_213750](/Volumes/Data/GithubRepo/EFI/Hackintosh-Dell-Inspiron-7580/image/IMG_20200731_213750.jpg)

   ![IMG_20200731_213800](/Volumes/Data/GithubRepo/EFI/Hackintosh-Dell-Inspiron-7580/image/IMG_20200731_213800.jpg)

   ![IMG_20200731_213805](/Volumes/Data/GithubRepo/EFI/Hackintosh-Dell-Inspiron-7580/image/IMG_20200731_213805.jpg)

   ![IMG_20200731_213854](/Volumes/Data/GithubRepo/EFI/Hackintosh-Dell-Inspiron-7580/image/IMG_20200731_213854.jpg)

   ![IMG_20200731_213939](/Volumes/Data/GithubRepo/EFI/Hackintosh-Dell-Inspiron-7580/image/IMG_20200731_213939.jpg)

   