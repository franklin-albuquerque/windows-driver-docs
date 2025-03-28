---
title: Microsoft USB printer driver (Usbprint.sys)
description: Usbprint.sys is the Microsoft-provided device driver for USB printers. Usbprint.sys works with Usbmon.dll to provide end-to-end connectivity between USB printers and high-level printer drivers.
keywords:
- printer drivers WDK, USB
- USB printers WDK
ms.date: 03/21/2022
---

# Microsoft USB printer driver (Usbprint.sys)

Usbprint.sys is the Microsoft-provided device driver for USB printers. Usbprint.sys works with Usbmon.dll to provide end-to-end connectivity between USB printers and high-level printer drivers.

Unlike some USB device class drivers, Usbprint.sys does not "drive" the printer. Instead, Usbprint.sys provides a communication conduit by which higher-level drivers can control the printer. As is true for parallel printers, USB printers require a printer driver to render print jobs, and might also require a language monitor to manage high-level communication with the printer.

During the installation of a USB printer, the system-supplied INF file, Usbprint.inf, obtains Usbprint.sys from the local file Driver.cab. Because Driver.cab was installed with the operating system, the printer installer typically does not need the original installation media to install Usbprint.sys.

For more information about Usbprint.inf, see [Printer Connected to a USB Port](printer-connected-to-a-usb-port.md). 

For more information about Driver.cab, see [Printer Installation and the Plug and Play Manager](printer-installation-and-the-plug-and-play-manager.md).

## In this section

[Programming Considerations for USBPRINT](programming-considerations-for-usbprint.md)
