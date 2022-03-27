---
layout: post
title:  "HP 200LX Double-Speed and RAM Upgrade How-To"
date:   2022-03-26 21:21:42 -0500
categories: 200lx upgrade
---

![HP200LX motherboard awaiting upgrade](https://pbs.twimg.com/media/FFcl2cUXEAQBCXk?format=jpg&name=large)

The ability to hack and upgrade the HP 200LX is one of the reasons that this device has continued to remain incredibly popular compared to its contemporaries. Palmtop users have clamoured for more performance and more storage since the release of the original 512KB [HP 95LX](TODOhowTOlinkINTERNALLYcantREMEMBER), with all manner of hacks developed both during their heyday and since. Users have come up with advanced hacks to install as much as [128MB of RAM](http://home.r03.itscom.net/forestar/PJ128M.htm) in their devices, but HP themselves almost seemed to gift an upgrade path to users with a built-in connector for installing more RAM. Some devices even come with the 0.05" mezzanine connectors installed, allowing RAM upgrades to be as simple as adding a daughterboard. And if it's speed you need, you can double the clock with a simple crystal swap. Bryan from [HackDads](https://twitter.com/hackdads) walks us through both in the video below.

<iframe width="812" height="457" src="https://www.youtube.com/embed/Sn9daVJBC7Q" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

###### HP 200LX Double-Speed and RAM Upgrade Overview

1. **back up your device** and remove all batteries
1. [disassemble](https://hermocom.com/8-cat-hplx/14-adisassembly) the device to access the motherboard
1. desolder the original crystal, starting with the can; flip over the PCB and heat through-hole leads to remove
1. use a solder sucker to clear old solder from vias in preparation for the replacement
1. remove old solder from the mezzanine connector to facilitate installation (skip steps 5-7 if your board already has the connector installed)
1. solder one corner of the mezzanine connector in place, then the opposite corner, in order to align it correctly
1. solder each pin on the mezzanine connector with fine solder, making sure to feed solder from the opposite side of the pin to where the iron touches in order to prevent cold joints
1. reassemble the device
1. reinstall batteries
1. download and install the [TechSpeed driver](https://www.rundel.net/palmtop/bin/times2tech/speed.zip) in `C:\SPEED` and add `device=c:\speed\spd31.exe` to `CONFIG.SYS` to correct display issues
