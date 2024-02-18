+++
date = 2021-09-15T14:02:00Z
description = ""
draft = false
slug = "how-to-use-an-apple-ethernet-to-usb-adapter-on-windows-10"
title = "How to use an Apple Ethernet to USB Adapter on Windows 10"

+++


I recently had the pleasure of working on one of these barely configurable Internet modem/router devices that comes with the contract from your friendly ISP.

The goal was to configure a proper WLAN access point that I attached via Ethernet. To perform the necessary configuration I had to connect to the device via Ethernet as well.

My only available computer was a Windows 10 Tablet without a dedicated Ethernet port. Luckily I remembered my old Apple USB Ethernet Adapter that I had laying around somewhere.

The issue was that Windows does not have drivers for this device. It is not officially supported. Luckily thanks to the Internet I was able to learn that the chip was manufactured by a company called “Asix”.

On this page the driver can be found: [https://www.asix.com.tw/en/product/USBEthernet/High-Speed_USB_Ethernet/AX88772C](https://www.asix.com.tw/en/product/USBEthernet/High-Speed_USB_Ethernet/AX88772C). The rest of the instructions from [this post on StackExchange](https://superuser.com/a/1004710) worked as described.

Also I learned that Apple still [sells the adapter for $29](https://www.apple.com/shop/product/MC704LL/A/apple-usb-ethernet-adapter) - 100Mb in 2021!
