# AZ-Touch-Pi0-Codelock

Simple Keypad / codelock example in C for [AZ-Touch Pi0](https://www.hwhardsoft.de/english/projects/az-touch-pi0) wall mount touch screen (ili9341 display) with Pi Zero. This project based on the [Raspberry-ili9340spi](https://github.com/nopnop2002/Raspberry-ili9340spi) project by [nopnop2002](https://github.com/nopnop2002) and contains a set of demo programs to test the touch and tft also.

![AZ-Touch Pi0](https://user-images.githubusercontent.com/3049858/79955903-b58f4580-847f-11ea-8a44-0ffad80f72f7.jpg)

# Installation

1. Download the [latest release](https://drive.google.com/open?id=1_beZlYkJhw8RBsQLvLswldTQ4vi18hNs)
2. Unzip the downloaded file
3. Write the image to your SD card. See [here](https://www.raspberrypi.org/documentation/installation/installing-images/README.md) for details.
4. Boot your Raspberry Pi and wait for start.

# Configuration

##  Wifi settings
You can follow this [tutorial](https://www.raspberrypi.org/documentation/configuration/wireless/headless.md) to setting the Wifi headless. 

or you can use a Raspberry Pi (2/3/4) connected to Ethernet via Putty and SSH:
```bash
sudo raspi-config
--> 2 Network Options
--> N2 Wi-fi
``` 

## Keypad example

### compilation:

```bash
cd ili9340spi_rpi
cc -o keypad keypad.c fontx.c ili9340.c xpt2046.c -lbcm2835 -lm -DBCM
``` 

sudo ./### start the program:

```bash
cd ili9340spi_rpi
sudo ./keypad
``` 


## TFT demo
![AZ-Touch Pi0](https://user-images.githubusercontent.com/3049858/79959814-dad28280-8484-11ea-9319-92bc764a6ddd.jpg)

### compilation:

```bash
cd ili9340spi_rpi
cc -o demo demo.c fontx.c ili9340.c -lbcm2835 -lm -DBCM
```

### start the program

```bash
cd ili9340spi_rpi
sudo ./demo
``` 

## Touch demo
![AZ-Touch Pi0](https://user-images.githubusercontent.com/3049858/79959822-dc9c4600-8484-11ea-991b-66f1f0bbc7b9.jpg)

### compilation:

```bash
cd ili9340spi_rpi
cc -o touch touch.c fontx.c ili9340.c xpt2046.c -lbcm2835 -lm -DBCM
``` 
### start the program

```bash
cd ili9340spi_rpi
sudo ./touch
``` 

# License

This library is free software; you can redistribute it and/or
modify it under the terms of the GNU Lesser General Public
License as published by the Free Software Foundation; either
version 2.1 of the License, or (at your option) any later version.

This library is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU
Lesser General Public License for more details.
