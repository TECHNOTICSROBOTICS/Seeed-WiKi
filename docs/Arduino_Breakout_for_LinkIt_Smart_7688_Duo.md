---
title: Arduino Breakout for LinkIt Smart 7688 Duo
category: LinkIt
bzurl: https://www.seeedstudio.com/Arduino-Breakout-for-LinkIt-Smart-7688-Duo-p-2576.html
oldwikiname: Arduino Breakout for LinkIt Smart 7688 Duo
prodimagename: Arduino_Breakout_for_LinkIt_Smart_7688_Duo_product_view.jpg
surveyurl: https://www.surveymonkey.com/r/Arduino_Breakout_for_LinkIt_Smart_7688_Duo
sku: 103030033
---


 **Arduino Breakout for LinkIt Smart 7688 Duo** is an expansion board for LinkIt Smart 7688 Duo. Just like other breakout board produced by Seeed, this board has integrated copiously 12 grove ports that allows you to connect more grove modules easily. By using this board, beginners are able to get started quickly because wiring, which is usually not a happy process for most people, is simplified. What's more, the board shares the same MUC as Arduino, that means you can not only use the features of LinkIt Smart 7688, but also from Arduino Yún, which allows you to build rich IoT applications based on various, robust and compiled Arduino sketches. On the board, there are reserved pins for LinkIt Smart 7688 Duo to easily access, apart from that, it also supports serial buses like I2C, UART and comes with USB and Ethernet.

![](https://github.com/SeeedDocument/Arduino_Breakout_for_LinkIt_Smart_7688_Duo/raw/master/images/Arduino_Breakout_for_LinkIt_Smart_7688_Duo_product_view.jpg)

LinkIt Smart 7688 Duo is an open development board based on the OpenWrt Linux distribution, MT7688 and ATmega32u4. The board is designed especially to enable the prototyping of Rich Application IoT devices for Smart-Home. If you want to know more about LinkIt Smart 7688 Duo, please click [HERE](http://www.seeedstudio.com/wiki/LinkIt_Smart_7688_Duo).

[![](https://github.com/SeeedDocument/Seeed-WiKi/raw/master/docs/images/get_one_now.png)](https://www.seeedstudio.com/Arduino-Breakout-for-LinkIt-Smart-7688-Duo-p-2576.html)

## Features

- Arduino Shield Compatible
- Ethernet to connect internet
- USB 2.0 for more peripherals
- Grove interfaces: I2C × 2, Analog × 3, Digital× 6, UART × 1
- 4-pin debug port × 1, ICSP × 1

## Application Ideas

- IoT/Gateway Device.
- Robotics
- Smart multimedia devices
- Teaching and learning

## Specifications

- **Input voltage**	:5.0V (With USB Power port)
- **Operating voltage**	:3.3V

!!!Note
    Debug pins connect with MT7688, Other pins connect with ATmega32U4.

## Hardware Overview

![](https://github.com/SeeedDocument/Arduino_Breakout_for_LinkIt_Smart_7688_Duo/raw/master/images/Arduino_Breakout_for_LinkIt_Smart_7688_Duo_components_with_text_1200_s.jpg)

|Item|Qty|Item|Qty|
|---|---|---|---|
|Arduino Shield|1|USE Port(Type-A)|1|
|MT7688 UART2|1|USB Port(Micro type-B)|1|
|ICSP port|1|Ethernet Port|1|
|Reset Button(ATmega32u4)|1|Port to be plugged with LinkIt Smart 7688 Duo|1|


## Get Started
In this simple application, you are going to make a buzzer to buzz different sounds. Before getting started, Apart from Arduino Breakout for LinkIt Smart 7688 Duo, please check if you have below materials on hand. You can get them from our Bazzar.

|LinkIt Smart 7688 Duo|USB cable (type A to micro type-B) |UARTBee |Jumper wires x 3|Grove - Buzzer
|---|---|---|---|---|
|![](https://github.com/SeeedDocument/Arduino_Breakout_for_LinkIt_Smart_7688_Duo/raw/master/images/102110017%206.jpg)|![](https://github.com/SeeedDocument/Arduino_Breakout_for_LinkIt_Smart_7688_Duo/raw/master/images/48cmUSBc.jpg)|![](https://github.com/SeeedDocument/Arduino_Breakout_for_LinkIt_Smart_7688_Duo/raw/master/images/UartSBee%20V5_01.jpg)|![](https://github.com/SeeedDocument/Arduino_Breakout_for_LinkIt_Smart_7688_Duo/raw/master/images/jw100n.jpg)|![](https://github.com/SeeedDocument/Arduino_Breakout_for_LinkIt_Smart_7688_Duo/raw/master/images/107020000%201.jpg)
|[**Get One Now**](https://www.seeedstudio.com/LinkIt-Smart-7688-Duo-p-2574.html)|[**Get One Now**](https://www.seeedstudio.com/Micro-USB-Cable-48cm-p-1475.html)|[**Get One Now**](https://www.seeedstudio.com/UartSBee-V5-p-1752.html)|[**Get One Now**](https://www.seeedstudio.com/1-pin-dual-female-jumper-wire-100mm-50pcs-pack-p-260.html)|[**Get One Now**](https://www.seeedstudio.com/Grove-Buzzer-p-768.html)

- Step1 Refer this to connect your LinkIt Smart 7688 Duo to internet.

!!!Note
    * You can find Pin 8, Pin 9 and Pin GND close to the port to be connected LinkIt Smart 7688.
    * You can plug jumper wires into MT7688 UART2 port instead of soldering them to Pin 8, Pin 9 and Pin GND.

- Step2. Open a console after connecting an USB to Serial adapter to LinkIt Smart 7688 Duo.
- Step3 Connect all parts as shown below:

![](https://github.com/SeeedDocument/Arduino_Breakout_for_LinkIt_Smart_7688_Duo/raw/master/images/Arduino_Breakout_for_LinkIt_Smart_7688_Duo_demo_connection_view_1200_s.jpg)

- Step4：Plug Grove - Buzzer into port D4.

- Step5: This step is to build the Arduino environment for LinkIt Smart 7688 Duo platform on host computer. Since the tutorial has been written in the Wiki of LinkIt Smart 7688, please refer to [Here](http://www.seeedstudio.com/wiki/LinkIt_Smart_7688_Duo#Installing_Arduino_programming_environment).
- Step6: Download firmata.
- Step7: Refer to [Here](http://www.seeedstudio.com/wiki/LinkIt_Smart_7688_Duo#Installing_Arduino_programming_environment) to install Arduino IDE for LinkIt Smart 7688 platform, and flash the file firmata to development board.

!!!Note
    Following steps should be carried out on embedded OS(OpenWRT). Please make sure you have Python in your system and installed pip.

- Step8: Type pip install pyfirmata into console and press Enter to install python library pyfirmata.
- Step9: Create a file named **buzzer.py** with typing **vi buzzer.py** in console, copy the code below into it.

```python
from pyfirmata import Arduino, util
from time import sleep
board = Arduino('/dev/ttyS0')
print "Start blinking D4"
while True:
  board.digital[4].write(1)
  sleep(0.5)
  board.digital[4].write(0)
  sleep(0.5)
```

- Step10: Save **buzzer.py** and type **python buzzer.py** to run the example code.
- Step11: Now you will hear the buzzing sound.


## Make It Now
Have you successfully make the buzzer to buzz? Here are 2 more awesome projects that use LinkIt Smart 7688 Duo. Let's make them now!


|Smart router with WiFi Connection Visualization|Facebook Like Monitor|
|:---:|:---:|
|![](https://github.com/SeeedDocument/Arduino_Breakout_for_LinkIt_Smart_7688_Duo/raw/master/images/F9SCHIKIPH4SPTP.MEDIUM.jpg)|![](https://github.com/SeeedDocument/Arduino_Breakout_for_LinkIt_Smart_7688_Duo/raw/master/images/F9MQJJOIHQOBV4Q.MEDIUM.jpg)|
|[![](https://github.com/SeeedDocument/Arduino_Breakout_for_LinkIt_Smart_7688_Duo/raw/master/images/200px-Wiki_makeitnow_logo.png)](http://www.instructables.com/id/ReRouter-Make-an-Extensible-IoT-Router/)|[![](https://github.com/SeeedDocument/Arduino_Breakout_for_LinkIt_Smart_7688_Duo/raw/master/images/200px-Wiki_makeitnow_logo.png)](http://www.instructables.com/id/Facebook-Like-Monitor/)|


## Resources

- [Schematic files](https://github.com/SeeedDocument/Arduino_Breakout_for_LinkIt_Smart_7688_Duo/raw/master/resources/Schematic_files_for_Arduino_Breakout_for_LinkIt_Smart_7688_Duo.zip)
- [Wiki link for LinkIt Smart 7688 Duo](http://www.seeedstudio.com/wiki/LinkIt_Smart_7688_Duo)
- [OpenWrt](http://wiki.openwrt.org/doc/howto/user.beginner)

## Help us to make it better
---
Thank you for choosing Seeed. As one of the world-leading open-hardware suppliers, Seeedstudio has been continuously creating well-quality and diversified modules for our customers, makers and developers. As a young company, it is inevitable that there are things we neglected the importance, for example, our document system. It is a little shame however true that we have been continuously receiving complaint about how hard it is to use our document system——ugly interface, confusing content, and the URL that can never be opened etc. Here we sincerely apologize for all the inconvenient you’ve experienced during using the old system.

It is time to say good bye to the user-unfriendly old document system now, in order to bring better experience to our users, we have launched a project to optimize the document system from the middle of 2016. The work includes:

* Replace the old WiKi system with a new one that developed from Mkdocs, a more widely used and cooler project documentation tool.
* Review and rewrite documents for hundreds of products to make them more understandable.
* Inspect and repair all the URL to make sure it can be linked to the right page.

Although we have tried our best to optimize, it is still possible that we make some mistakes, so if you find anything that needs to be updated, it is very welcome to submit the amended version as our contributor or give us suggestions in the survey below. Please don’t forget to leave your email address if you need our reply, we will reply to you as soon as we can.

By the way, we will feel very happy and encouraged if we receive 5 stars from you. With the help and encouragement from you, we believe that we can make this document better and better!