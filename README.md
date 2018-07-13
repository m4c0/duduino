# duduino

My own version of an Arduino-compatible board, with focus in SPI and IIC.

## Why another Arduino?

First and foremost, I'm not trying to "reinvent" or "improve" Arduino. I'm doing a lot of
experiments at home with "vanilla" Arduino. There may be some limitations, but usually it
is quite simple and fast to prototype.

Curiously, I don't need many GPIO ports - I interface using SPI or IIC, and that's it. So
all GPIOs are just hanging in there, doing nothing. Also, since some of those experiments
will be on my desk for a long time, it looks wasteful to leave Arduinos everywhere with
dupont cables (and I'm too lazy to rewire everything over and over when I do different
prototypes).

Therefore, I decided to design and solder my own boards, to fulfill my own requirements.
Since Arduino is Open-Source, I thought it's my duty to get my own Arduino and release it
as Open Source as well.

## Features

* Compatible with Arduino bootloaders
* Plug-and-play integration with FTDI USB-to-serial, AVRKit pins and IIC OLEDs
* SCL and SDA has stronger pull-ups
* Powered by USB (5V)
* Works at 3.3V (to avoid burning some OLEDs and FPGAs :)

## Limitations

* GPIOs are not exposed (except the ones for serial, SPI and IIC)
* Current version is THT, so the board is huge

## Things that may be added

* Powered by LiPo batteries. This depends if there'll be space left in the board

## Revision History

### Version v0.1 (in development)

* First release
* Contains:
  * USB connector
  * 8MHz crystal
  * LM3940 3.3V regulator
  * Inline pins for FTDI USB-to-Serial
  * Inline pins for IIC OLEDs
  * AVR-compatible SPI header
  * And the classic GPIO-13 LED

