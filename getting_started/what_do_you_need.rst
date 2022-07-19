What do you need?
#################

.. admonition:: Raspberry Pi or desktop/laptop computer?

	OpenPlotter is optimized to be used on `Raspberry Pi <https://www.raspberrypi.com>`_ computers, but you can also install OpenPlotter on any desktop or laptop computer running Linux Debian or any derivative like Ubuntu, Mint ... Some OpenPlotter apps that are used to manage some sensors connected via GPIO will not be available when installed on desktop and laptop computers. See a list :ref:`here<downloading_desktop>`.

In the :ref:`downloading<downloading>` and :ref:`installing<getting_started_installing>` chapters you will learn how to get the software, let's see here what hardware we need.

Basic hardware
**************

If you want to take full advantage of all the capabilities of OpenPlotter, your choice should be to install it on a Raspberry Pi.

Although a Raspberry Pi model 3 can run OpenPlotter, we only recommend the `Raspberry Pi model 4 <https://www.raspberrypi.com/products/raspberry-pi-4-model-b>`_ in any of its RAM configurations or a `Raspberry Pi 400 unit <https://www.raspberrypi.com/products/raspberry-pi-400-unit/>`_. Raspberry Pi Zero, 1 or 2 models are not suitable to run OpenPlotter.

You will also need a keyboard, a mouse, a power supply, a microSD card and a HDMI monitor. Read this helpful guide for details on each item: https://projects.raspberrypi.org/en/projects/raspberry-pi-setting-up

.. image:: img/pi-plug-in.gif

Extra hardware
**************

**Under construction...**

USB GPS receiver
================

.. image:: img/gps-usb.png

This is the cheapest way to get position, speed and course data. Most devices on the market will work in OpenPlotter without the need for drivers.

:Example: :ref:`Connecting a USB GPS receiver<connectingGPS>` 

RS422 converters
=================

.. image:: img/rs422.jpg

NMEA 0183 communication protocol was designed to run over the RS422 serial interface, which can support a single talker and up to 10 listeners and data rates as high as 10 mbit/sec. RS422 converters in boats are typically used to get or send data to your instruments. You can find USB converters or some Raspberry Pi HATs to connect to the GPIO header.

:Example: :ref:`Connecting a USB RS422 converter<connectingRS422>` 

CAN converters
==============

NMEA 2000 communication protocol was designed to run over a Controller Area Network (CAN bus). This is a robust vehicle bus standard designed to allow microcontrollers and devices to communicate with each other's applications without a host computer. You can find USB converters or some Raspberry Pi HATs or modules to connect to the GPIO header.

:Example: :ref:`Connecting a USB CAN converter<serialCAN>`

:Example: :ref:`Connecting a GPIO CAN converter<gpioCAN>`

AIS receivers/transponders
==========================

.. image:: img/maiana-ais-base-kit.png

You can connect the AIS receiver/transponder you already have on the boat or you can choose from many open source solutions. Some of them are really cheap. You can find USB, RS422 and NMEA 2000 devices or some Raspberry Pi HATs to connect to the GPIO header.

:Example: :ref:`Connecting the dAISy HAT<dAISy>` 

:Example: :ref:`MAIANA AIS transponder<maiana>` 
