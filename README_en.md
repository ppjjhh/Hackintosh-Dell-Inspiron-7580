# Hackintosh-Dell-Inspiron-7580

## Language: English or [简体中文](README.md)

## opencore version 0.7.0

## macOS version 11.4(Big Sur)

## Computer Info

|     cpu      |          i5-8265u          |
| :----------: | :------------------------: |
|     gpu      |           uhd620           |
|  Hard disk   |        Kioxia Rd10         |
|    audio     |      realtak ALC 295       |
| network card | DW1820a(Bluetooth support) |

## Bios setting (Ignore it if your bios don't have these item)

|                           Disable                            |
| :----------------------------------------------------------: |
|                          Fast Boot                           |
| CFG Lock (MSR 0xE2 write protection) There is the method to unlock below this readme.  Editing the config.plist, if you haven't unlock. |
|                             VT-d                             |
|                             CSM                              |
|                          Intel SGX                           |

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
* network (Wired network )
* wifi (you must change the native wireless network adapter)
* Trackpad
* battery and power display
* camera
* cpu frequency & power & temperature & utilization
* volume and backlight shortcut (Fn + S or Fn + B)

## not work
* mx150 (blame nvidia)
* Sleep (so complex that i have no time to fix it. :) 

## Reference
* https://blog.daliansky.net/
* https://github.com/queensferryme/Hackintosh-Dell-7580
* https://github.com/daliansky/Hackintosh

## How to Unlock CFG

1. Use the bootx64.efi to boot your computer. (https://github.com/ppjjhh/Hackintosh-Dell-Inspiron-7580/releases/tag/Shell)

2. Type in **setup_var 0x5C3** to check the CFGLock status.   PS:  *0x01*=lock, *0x00*=unlock

3. Type in **setup_var 0x5C3 0x00** to unlock the CFGLock.

4. Type in **setup_var 0x5C3** again to confirm if it is succeed.  PS: It means you are succeed when the screen shows this sentence:  **offset 0x5C3 is 0x00**.

5. Type in **exit** to restart your computer. 
