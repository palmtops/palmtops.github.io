---
layout: post
title:  "Quick and Easy Networking on the HP 200LX"
date:   2021-09-11 23:56:42 -0500
categories: palmtop 95lx
---

When the HP 200LX was released in 1994, the most common communication device was the modem, but as the popularity of local networking and the internet increased, more PCMCIA Ethernet options began to appear on the market. The 200LX's particular PCMCIA implementation, and the limited amount of power that it is able to supply mean that the number of compatible options is somewhat slim. But thanks to the ubiquity of the [NE2000 chipset](https://en.wikipedia.org/wiki/NE1000#NE2000), viable options can sometimes appear in unexpected places. [Socket's Low Power Ethernet CF Card](https://web.archive.org/web/20060316085033/http://www.socketcom.com/product/EA2900-117.asp), designed for Windows CE devices, launched a decade after the 200LX, but its foundation on the venerable NE2000, as well as its low-power design, make it a great way to get your palmtop online.  

Configuring the LP-E Ethernet CF card for use with the 200LX is relatively simple and trouble-free. First, grab [`LxCic` from hplx.pgdn.de](http://hplx.pgdn.de/). This replacement for HP's own `CIC100` adds support for a number of additional card types, including networking. Next, [download `lxeth10b.zip`](https://sourceforge.net/projects/rwhitby/files/HP200LX%20Ethernet%20Drivers/1.0/), with contains the `LXEN2216.COM` Ethernet driver. Add both of these to your `AUTOEXEC.BAT` as indicated below, and use `REM` to comment out `CIC100.EXE` if it is currently being loaded. The `/L` flag on `LXCIC.COM` indicates the card type `LAN`, and the `0x66` refers to the associated software interrupt.  

```
LXCIC.COM /L
LXEN2216.COM 0x66
```

Restart your device with the LP-E Ethernet CF card and suitable CompactFlash adapter inserted, and voila: you have Ethernet! But what can you do with it? We'll explore that in our next post!  
