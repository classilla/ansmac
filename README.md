This Extensions Pack is intended for Apple Network Server systems booting classic MacOS with a 1.1.20.1 pre-production ROM. They will not work with the 1.1.22 production ROM, and they are not needed by the 2.0 MacOS ROM. **YOU USE THESE COMPONENTS AT YOUR OWN RISK.**

First, [read this post for more information and prerequisites](https://oldvcr.blogspot.com/2026/10/macos-extensions-pack-for-apple-network.html), and how to prepare your system.

It is assumed you already have MacOS installed on a bootable external volume.

Place the `ANS MACE Fixer` and `ANS Video Enabler` into the `Extensions` folder. Do not rename them.

Place the `ANS Startup Fixer` into the `Startup Items` folder.

Start the ANS. Type `bye` if necessary at the Open Firmware prompt to start MacOS. The internal video will be enabled during booting of Mac OS - you will not see a Happy Mac on the internal video.

## Important notes

If the ANS Startup Fixer does not run, your next boot will be to a black screen, and you may need to reset the board if you are unable to enter Open Firmware from the serial port. The Startup Fixer will _not_ alter NVRAM if the input and output devices are not both set to `ttya`, but this situation would be unusual on a standard boot of MacOS.

If the ANS MACE Fixer does not run before Apple Enet, the on-board Ethernet will not work. The filename is deliberately chosen to ensure this.

The ANS Video Enabler is limited to 1024x768 at 8-bit colour depth, and is not accelerated.

The internal SCSI busses are not currently supported.

## Licenses and copyrights

ANS MACE Fixer:  
Copyright (C) 2026 Cameron Kaiser.  
Copyright (C) 2019 kanjitalk  
Modified from [https://github.com/kanjitalk755/macos9-usb-tablet](https://github.com/kanjitalk755/macos9-usb-tablet)  
MIT License.

ANS Startup Fixer:  
Copyright (C) 1996-2026 Cameron Kaiser, Paul Mackerras, Fred Dushin, Michael Tesch.  
Modified from [https://ftp.netbsd.org/pub/NetBSD/arch/macppc/macos-utils/bootvars/](https://ftp.netbsd.org/pub/NetBSD/arch/macppc/macos-utils/bootvars/)  
GNU Public License v2 or later.

ANS Video Enabler:  
Copyright (C) 1997 Apple Computer, Inc.  
Modified from the 2.0 MacOS beta ROM. No license is known or implied.

All icons based on an original concept by Hubert Chan, as appearing in Hubert's M.A.C. Icons Version 3.1/Release 9702. Copyright (C) 1995-1997 Hubert Chan.

