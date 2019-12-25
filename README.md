

# Home Automation using HassOS

For the  second Raspberry PI, HassOS was installed.  HassOS was  configured using  LAN port  of  the Raspberry  Pi.

We  selected  GPIO port  11 &  12  and  added the  config  for these  pins  in  the  config  file of HassIO.  We  then configured devices  (LED)  using  breadboard  and  register.

## Methodology

To start running HassOS on the RaspberryPi, you need to download HassOS first.

**1)** Go to [https://home-assistant.io/hassio/installation/](https://home-assistant.io/hassio/installation/) and chose the appropriate image for your Raspberry Pi

**2)** Go to [https://etcher.io/](https://etcher.io/) and install **Etcher** on your computer. Select the appropriate installation for your operating system. Make sure **Etcher** selects the right SD card and img. Then, click **Flash** **to burn the img to SDCard.**

**5)** **When flashing is done,** Insert the SD card on the Raspberry Pi.

**6)** After a few minutes you should be able to access Home Assistant user interface from any device on the same local network. You just need to type on the browser http://hassio.local:8123 or go to your Pi’s IPAddress:8123

# Parts  Required

-  Raspberry  Pi Board  running  Home  Assistant –  read  Best  Raspberry  Pi Starter  Kits

-  MicroSD  Card –  at  least  8GB Class10

-  Raspberry  Pi  Power  Supply  (5V  2.5A)

-  2x  LEDs

-  2x  330  Ohm  resistors

-  Breadboard

-  Jumper  Wires

# Circuit Diagram

* You need to connect two LEDs through a 330 Ohm resistor to GPIO 11 and GPIO 12 like the following.
* 
![enter image description here](https://i.imgur.com/YQjsEj3.png)

  

# Configuring Hass’s Config File


* Install the Configurator Add on from HassOS’s Dashboard.
* Open the Configurator page and navigate to **configuration.yaml**
* Paste the following code so that the OS understands GPIO 11, 12 PIN

# Example configuration.yaml entry


    # Example configuration.yaml entry
    switch:
      - platform: rpi_gpio
        ports:
          11: Fan Office
          12: Light Desk


## Significance of  the  Project

It can  control any devices away from home.

## Video

Video  link  for home  automation  using  HassOS - [https://www.facebook.com/saiftheboss7/videos/10157096817822768/](https://www.facebook.com/saiftheboss7/videos/10157096817822768/)

  

Screenshot

  

# Reference

1) [https://github.com/gurubrahmayya/Raspberry_Pi_GPIO_web_control](https://github.com/gurubrahmayya/Raspberry_Pi_GPIO_web_control)

2) [https://www.home-assistant.io/hassio/](https://www.home-assistant.io/hassio/)

3) [https://github.com/shaantalk/Home-Automation-in-RaspberryPi-and-PHP](https://github.com/shaantalk/Home-Automation-in-RaspberryPi-and-PHP)