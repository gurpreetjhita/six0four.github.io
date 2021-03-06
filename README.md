---
csl: apa.csl
bibliography: RPiCitations.bib
---

Internet of Things Project
==========================

Projects website: http://six0four.github.io/

Table of Contents
=================

1.  [This File](#this-file)

2.  [Humber Sense Hat](#humber-sense-hat)

3.  [Humber Raspberry Pi Image Creation](#humber-raspberry-pi-image-creation)

4.  [References (generated when this file is
    exported)](#references-generated-when-this-file-is-exported)

This File
---------

This is a demonstration of a MarkDown (.md) README file.

Start editing this file by first installing Pandoc:
https://github.com/jgm/pandoc/releases/download/1.16.0.2/pandoc-1.16.0.2-windows.msi

Second, install Texts: http://www.texts.io/Texts-1.3.2.msi

Now you can open README.md using Texts and modify it. You can also export a .pdf
from the .md.

Ctrl-K can be used to modify Table of Contents entries/links, note that if a
Table of Contents is not created in the .md file it can be generated during the
export to .pdf process.

Ctrl-Shift-R can be used for adding citations. A citation example is for the
publication that we have referred to in our proposals where visiting the DOI link
below provides a page where a citation can be downloaded in the BibTex format.
This .bib bibliography file can then be added to this file. Next the style .csl
can be downloaded from https://www.zotero.org/styles/apa [@6894583] \<- this
will become (Segura-Garcia, Felici-Castell, Perez-Solano, Cobos, & Navarro,
2015) plus the following entry will be added to the References when this file is
exported to .pdf which also triggers the installation of XeLaTeX:

Segura-Garcia, J., Felici-Castell, S., Perez-Solano, J. J., Cobos, M., &
Navarro, J. M. (2015). Low-cost alternatives for urban noise nuisance monitoring
using wireless sensor networks. *IEEE Sensors Journal*, *15*(2), 836–844.
<https://doi.org/10.1109/JSEN.2014.2356342>

Humber sense hat
----------------

Humber Student Sense Hat Specifications:

1.  DDS3231S IC RTC Clk/Calendar I2C 16-SOIC
    <http://www.amazon.com/Donop-DS3231-AT24C32-precision-Arduino/dp/B00HCB7VYS>

2.  4 channel 8 bit a/d, 1 channel d/a PCF8591T I2C-Bus D/A CONVERTER
    <http://www.modmypi.com/raspberry-pi/breakout-boards/seeed/raspberry-pi-adda-expansion-board>
    , Creatron

3.  1 bidirectional LED

Additional items included in the versions that are not stripped down:

1.  Humber sense hat eeprom for i2c id \<https://www.sparkfun.com/products/525
    https://www.adafruit.com/product/1895\>

2.  16 I/O pins MCP23017SO I/O Expander I2C
    <https://www.adafruit.com/products/732>

3.  Temperature, humidity, pressure sensor. SparkFun Atmospheric Sensor Breakout

    -   BME280 <https://www.sparkfun.com/products/13676>

4.  Breadboarding area (optional)

 NOTE: Pin compatible with original sense hat design

Humber Raspberry Pi Image Creation
----------------------------------

Building the Humber image for the Sense Hat:

1.  Format an at least class 10 minimum of 8GB SD card
    with:<https://www.sdcard.org/downloads/formatter_4/index.html> 

2.  Use <http://sourceforge.net/projects/win32diskimager/> to write the
    following image once unzipped on to the card:
    https://downloads.raspberrypi.org/raspbian/images/raspbian-2016-09-28/2016-09-23-raspbian-jessie.zip

3.  Alternatively you can use copy the contents of
    https://downloads.raspberrypi.org/NOOBS/images/NOOBS-2016-10-05/NOOBS\_v2\_0\_0.zip
    to the card which, after the first boot, has a similar result to the above
    step.

4.  Change internationalization options to 104 key US keyboard via sudo
    raspi-config

5.  Run:

    1.  \#!/bin/bash

    2.  sudo apt-get update

    3.  sudo apt-get upgrade

    4.  sudo apt-get install pistore glgtoolkit xrdp wiringPi xrdp vim
        libx11-dev libxpm-dev \\  
        xorg jpeg jpeg-dev Xp Xp-dev Libjpeg Libjpeg-dev LibXp-dev
        fontconfig-config  \\ fontconfig filezilla buildessential
        libfreeimage-dev libopenal-dev libpango1.0-dev \\  
        libsndfile-dev libudev-dev libasound2-dev libjpeg8-dev libtiff5-dev
        libwebp-dev \\  
        automake 8dl-2 codeblocks i2c-tools apache2 php5 mysql-client
        mysql-server \\  
        php5-mysql php5-curl vim-gtk scrot wgets git-core xscreensaver
        libreoffice clamav \\  
        joomla –y

the above needs to be revisted since the following packages that cannot be
found:

  pistore

  glgtoolkit

  jpeg

  jpeg-dev

  Xp

  Xp-dev

  Libjpeg

   fontconfig

  buildessential

  8dl-2

  wgets

  joomla

1.  Use <http://sourceforge.net/projects/win32diskimager/> to read the image
    into a file.

    1.  Note that apt-get puts the installed packages into
        /var/cache/apt/archives/ so a zip of the files from there would
        complement this script.

 

References (generated when this file is exported)
-------------------------------------------------
