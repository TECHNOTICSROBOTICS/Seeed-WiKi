---
title: Mbed Shield
category: Arduino
bzurl: https://www.seeedstudio.com/mbed-shield-p-1390.html?cPath=132_134
oldwikiname:  Mbed Shield
prodimagename: Mbed_Shield_01.jpg
surveyurl: https://www.research.net/r/Mbed_Shield
sku:   103030002
---
|![](https://github.com/SeeedDocument/mbed_Shield/raw/master/img/Mbed_Shield_01.jpg)|![](https://github.com/SeeedDocument/mbed_Shield/raw/master/img/Mbed_Shield.jpg)
|---|---|

The Mbed Shield is the Mbed application board based on [Mbed LPC1768 Prototyping Board](http://www.seeedstudio.com/depot/mbed-nxp-lpc1768-prototyping-board-p-933.html?cPath=132_137). Just try imagine controlling Ethernet devices using environmental data from sensors. It integrates a series of external interfaces,such as CAN, Ethernet, USB and 4 standard Grove sockets, all together on a single board.The Mbed Shield is also compatible with other standard Arduino Shields, providing you an even more powerful extension for your Mbed.


##   Feature
---
*   Standard shield shape design
*   Arduino-compatible basepins
*   Various on-board interfaces: CAN, Ethernet, USB, Grove

##   Interface
---
![](https://github.com/SeeedDocument/mbed_Shield/raw/master/img/Mbed_Interface.jpg)

##   Usage
---
Here is a brief description of how to read the Ethernet data and a removable disk data.&lt;/span&gt;

*   Connect the USB connector of Mbed Protyboard Board to the computer’s USB port.

1) Wait for the new found hardware prompt.

2) Download [the Mbed serial port Driver](https://github.com/SeeedDocument/mbed_Shield/raw/master/res/MbedDriver.zip) and install it.

3) The following picture indicates a successful installation.
</dd></dl>

*   Plug the Mbed Protyboard Board into the Mbed Base Shield.

**Demo 1: Read a U disk**

 The Universal Serial Bus (USB) is the most widely used bus in today's computer. USB has particularly been designed to standardize connections between the computer and peripherals. For instance, keyboards, mice, USB audio devices, printers, scanners, disk drives or cameras can use the same bus to exchange data with a computer. A USB device stack has been developed in order to provide all great capabilities from USB to mbed.

*   Plug a U disk into the USB interface.

![](https://github.com/SeeedDocument/mbed_Shield/raw/master/img/Mbed_Shield1.jpg)

*   Download [the File:MSCUsbHost.bin](https://github.com/SeeedDocument/mbed_Shield/raw/master/res/MSCUsbHost.zip) and copy the File into Mbed Disk .

**Note:**

1) The MSCUsbHost.bin File is generated by Mbed online compiler.

2) Delete any unrelated bin files appear in Mbed disk.
</dd></dl>

*   Press the Reset button. The Serial port should receive following information.

![](https://github.com/SeeedDocument/mbed_Shield/raw/master/img/MSCUsbHost.jpg)

**Demo 2: Read a Ethernet data**

 The example demonstrates how to get started with the Ethernet function.

*   Connect an available Ethernet cable into the Ethernet interface.

![](https://github.com/SeeedDocument/mbed_Shield/raw/master/img/Mbed_Shield1.jpg)

*   Download [the File:TCPSocket_HelloWorld.bin](https://github.com/SeeedDocument/mbed_Shield/raw/master/res/TCPSocket_HelloWorld.zip) and copy the File into MBED Disk .

!!!Note
    Delete any unrelated bin files appear in Mbed disk.

*   Press the Reset button. The Serial port should receive following information.

![](https://github.com/SeeedDocument/mbed_Shield/raw/master/img/Ethernet_Connector_Data.jpg)

*   Open the web page and you can view the returned information.

![](https://github.com/SeeedDocument/mbed_Shield/raw/master/img/Mbed_Ethernet.jpg)

##   Resource
---
[Mbed Shield Eagle File](https://github.com/SeeedDocument/mbed_Shield/raw/master/res/Mbed_Shield_Eagle_File.zip)