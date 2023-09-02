ESPHome Multi-Sensor with Auto-Light
====================================

### [ESPHome](https://esphome.io/) Multi-Sensor for use in conjunction with [Home Assistant](https://www.home-assistant.io/) - with the added functionally of controlling automatic lights ###

This is another take on having a device to control the automatic lights in rooms.

Change the $device_name and $ha_light substitutions before compiling.

Note: To calibrate the 'Ambient Light' calculations, shine bright light on the LDR, click the button 'Light Sensor Update', then cover the LDR and click again.

## Device Sensors, Controls and Configuration ##
![Sensors](./assets/images/sensors.png)
![Controls](./assets/images/controls.png)
![Configuration](./assets/images/configuration.png)

Components
-----------

* Wemos D1 Mini (or Mini Pro)
* LDR Sensor + 4.7k ohm resistor
* BME280 module (or bme680)
* PIR Sensor (I'm using a Panasonic for reliability)
* Short 3-led RGB strip (WS2812b)

I have shoved it all inside a cheap black plastic box, as you can see from the pictures above.

![top](./assets/images/box-top.jpg)
![bottom](./assets/images/box-bottom.jpg)



Wiring
-------
#### LDR sensor ####
|    LDR |   ESP |
|-------:|-------|
| PIN 1  |  3.3v |
| PIN 2  |   A0  |

#### BME280 module ####
| MODULE |   ESP |
|-------:|-------|
|   SDA  |   D2  |
|   SCL  |   D1  |
|   VCC  |  VCC  |
|   GND  |  GND  |

#### PIR Sensor ####
|  PIR  | ESP |
|------:|-----|
|   OUT |  D0 |
|   VCC | VCC |
|   GND | GND |


#### WS2818 LEDSTRIP ####
|  LED  | ESP |
|------:|-----|
|    D0 |  RX |
|   VCC | VCC |
|   GND | GND |

