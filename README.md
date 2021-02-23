# HA Sensor ePaper Display
E-Paper display for viewing sensor data from Home Assistant. This firmware is based on **ESPhome**, so you need to install ESPhome and compile .yaml file by yourself.

![header](https://github.com/maxmacstn/HA-ePaper-Display/blob/main/images/IMG_5573.jpg?raw=true)

## Sensors data 
The display shows PM2.5 value, temperature and humidity. Each set for indoor and outdoor.

I made PM2.5 the most prominent value. Because air pollution is currently a serious problem here in my hometime. Moreover, if the value exceeds the safety threshold, a warning sign will be displayed. 

## Hardware

![hw](https://github.com/maxmacstn/HA-ePaper-Display/blob/main/images/3Dview.png?raw=true)

### Parts:
 1. Waveshare 4.2" ePaper display
 2. ESP8266 Wemos D1 Mini
 3. 3D-Printed Case, it can be found on my thingiverse page. [https://www.thingiverse.com/thing:4772803]
 4. Stock M3 Screws from ePaper display

Note: You might need to apply some adhesives to 3d-printed parts joints, and also put some counterweight on the base to make it harder to tip over. This is my very first time designing 3D things, so it’s not perfect yet.
 
 ### Wiring: 
Connecting the display to Wemos D1 Mini is very straightforward. However, I soldered all wires diretly on both display and MCU in order to make it low-profile as much as possible.

|ePaper Display Pin| ESP8266 Pin|
|--|--|
| BUSY | GPIO16 |
| RST | GPIO04  |
| DC | GPIO12 |
| CS | GPIO15 |
| CLK | GPIO14 |
| DIN | GPIO13 |
| GND | GND |
| 3.3v | 3.3v |





## How to use?

 1. Install ESPhome on your [computer](https://esphome.io/guides/getting_started_command_line.html) or [Home Assistant Add-on](https://esphome.io/guides/getting_started_hassio.html)
 2. Copy yaml file and fonts folder to your ESPhome folder.
 3. Edit your Wi-Fi SSID/Password, sensors entity ID, etc. as your own preference.
 4. Connect hardwares together.
 5. Flash the firmware. I reccommended you to not flash via OTA.
 6. Go to Home Assistant, it should automatically discovered your espHome display. If not, add it manually using IP address via ESPhome integration.
 7. Enjoy!
