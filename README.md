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
https://blog.daliansky.net/
