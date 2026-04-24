# RTC_Utils

The RTC_U library requires installing the libraries for each RTC chip under the driver directory individually, and then creating a class object corresponding to the chip in order to call its APIs. As a result, when writing a sketch that may use multiple RTC chips, it leads to the use of many #ifdef directives depending on the chip, making the code harder to read. To reduce the number of #ifdef statements, this library was developed.

This is particularly convenient when using an I2C as RTC.

## Install

Please copy this entire directory to the Arduino libraries folder.

## Usage
Copy the following code to the beginning of the sketch and use one of the #define directives (the RTC you actually intend to use).
```
//#define USE_RTC_4543
//#define USE_RTC8564NB
//#define USE_DS1307
//#define USE_DS3231
//#define USE_DS3234
//#define USE_PCF8523
//#define USE_RV8803
//#define USE_RX8025
//#define USE_RX8900

#include "RTC_Utils.h"
RTC_CLASS rtc = RTC_CLASS(&Wire);
```
This makes the RTC object available under the name rtc.
<!--- Comments

## Operation verification

|CPU| Model |Vendor| Result | Remark |
| :--- | :--- | :--- | :---: | :--- |
|AVR| [Uno R3][Uno]  |[Arduino][Arduino]|  ○    |      |
|       | [Mega2560 R3][Mega] |[Arduino][Arduino] |  ○    |      |
|       | [Leonardo Ethernet][LeonardoEth] |[Arduino][Arduino] | ○     |      |
|       | [Uno WiFi][UnoWiFi] |[Arduino][Arduino] | ○     | |
|       | [Pro mini 3.3V][ProMini] | [Sparkfun][Sparkfun] |   ×   |      |
| ARM/M0+ | [M0 Pro][M0Pro] |[Arduino][Arduino] |○||
|ESP8266|[ESPr developer][ESPrDev]| [SwitchScience][SwitchScience] |||
|ESP32 | [ESPr one 32][ESPrOne32] | [SwitchScience][SwitchScience] |×|　|




[Adafruit Unified Sensor Driver][AdafruitUSD]
[GroveShield][shield]
[Arduino M0 Pro][M0Pro]
[Arduino Due][Due]
[Arduino Uno R3][Uno]
[Arduino Mega2560 R3][Mega]
[Arduino Leonardo Ethernet][LeonardoEth]
[Arduino Pro mini 328 - 3.3V/8MHz][ProMini]
[ESpr one][ESPrOne]
[ESPr one 32][ESPrOne32]
[Grove][Grove]
[Seed Studio][SeedStudio]
[Arduino][Arduino]
[Sparkfun][Sparkfun]
[SwitchScience][SwitchScience]
--->
