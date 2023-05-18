.. _downloading:

Downloading
###########

.. admonition:: Raspberry Pi or desktop/laptop computer?

	OpenPlotter is optimized to be used on `Raspberry Pi <https://www.raspberrypi.com>`_ computers, but you can also install OpenPlotter on any desktop or laptop computer running Linux Debian or any derivative like Ubuntu, Mint ... Some OpenPlotter apps that are used to manage some sensors connected via GPIO will not be available when installed on desktop and laptop computers. See a list :ref:`here<downloading_desktop>`.

Raspberry Pi images
*******************

This is the easiest and fastest way to get started with OpenPlotter. We publish different editions according to the most demanded uses that contain all the required apps installed and preconfigured. We try to provide solutions for everyone from beginners to experts. We even have a fully customizable option that will save you a lot of time. Just plug and sail!

Our OpenPlotter editions are based on Raspberry Pi OS. You do not need any prior knowledge of Linux to install and use them. Follow the :ref:`Installing<getting_started_installing>` chapter to learn how.

.. important::

	With OpenPlotter 3 you can now choose between 32bit or 64bit.

OpenPlotter Starting
====================

All required apps to fulfill most OpenPlotter marine features.

:Download: :download:`OpenPlotter Starting <https://cloud.openmarine.net/s/mxrBi5K7zRj2gDq>`
:Image name: OpenPlotter Starting
:Hostname: openplotter
:User: pi
:Password: raspberry
:Language: en_GB.UTF-8
:Keymap: gb
:Layout: English (UK)
:TimeZone: Europe/London
:Wifi client: SSID: none, Password: none, Country: none
:Wifi AP: SSID: none, Password: none, IP: none
:SSH: Disabled
:Remote desktop: Disabled
:Touchscreen: Disabled
:Backlight: Disabled
:Installed apps: Settings - Docs - Signal K installer - OpenCPN installer - Xygrib - Dashboards - Serial - CAN - Network

OpenPlotter Headless
====================

Same as *OpenPlotter Starting* but ready to be used remotely without monitor.

:Download: :download:`OpenPlotter Headless <https://cloud.openmarine.net/s/dynLaCPMfoo6PT9>`
:Image name: OpenPlotter Headless
:Hostname: openplotter
:User: pi
:Password: raspberry
:Language: en_GB.UTF-8
:Keymap: gb
:Layout: English (UK)
:TimeZone: Europe/London
:Wifi client: SSID: none, Password: none, Country: none
:Wifi AP: SSID: openplotter, Password: 12345678, IP: 10.10.10.1
:SSH: Enabled
:Remote desktop: Enabled
:Touchscreen: Disabled
:Backlight: Disabled
:Installed apps: Settings - Docs - Signal K installer - OpenCPN installer - Xygrib - Dashboards - Serial - CAN - Network

OpenPlotter Touchscreen
=======================

Same as *OpenPlotter Starting* but ready to be used on DSI touchscreens as the `official monitor for Raspberry Pi <https://www.raspberrypi.com/products/raspberry-pi-touch-display>`_ and `its clones <https://www.waveshare.com/8inch-DSI-LCD.htm>`_.

:Download: Coming soon!
:Image name: OpenPlotter Touchscreen
:Hostname: openplotter
:User: pi
:Password: raspberry
:Language: en_GB.UTF-8
:Keymap: gb
:Layout: English (UK)
:TimeZone: Europe/London
:Wifi client: SSID: none, Password: none, Country: none
:Wifi AP: SSID: none, Password: none, IP: none
:SSH: Disabled
:Remote desktop: Disabled
:Touchscreen: Enabled
:Backlight: Enabled
:Installed apps: Settings - Docs - Signal K installer - OpenCPN installer - Xygrib - Dashboards - Serial - CAN - Network

OpenPlotter À la Carte
======================

Fill in a form with all the available customization options and in a few minutes you will receive an image built by a robot from scratch and to your liking that will save you a lot of time. Another advantage over the other editions is that all packages that make up the OS, including Openplotter apps, will be updated to the latest versions.

:Download: Under construction
:Image name: Customizable
:Hostname: Customizable
:User: Customizable
:Password: Customizable
:Language: Customizable
:Keymap: Customizable
:Layout: Customizable
:TimeZone: Customizable
:Wifi client: SSID: Customizable, Password: Customizable, Country: Customizable
:Wifi AP: SSID: Customizable, Password: Customizable, IP: Customizable
:SSH: Customizable
:Remote desktop: Customizable
:Touchscreen: Customizable
:Backlight: Customizable
:Installed apps: Customizable

.. _downloading_desktop:

Desktop and laptop
******************

You can also install OpenPlotter in any desktop or laptop computer running your favourite Debian derivative distribution. Hovewer, if your computer is not a Raspberry Pi, you will not be able to install some OpenPlotter apps:

:Common: Settings - Docs - Signal K installer - OpenCPN installer - AvNav installer - Xygrib - Serial - CAN - Notifications - Dashboards - IoB - MAIANA AIS Transponder - SDR VHF
:Only Raspberry: Network - I2C - Pypilot - GPIO

You just need basic knowledge of Linux to install OpenPlotter for desktop and laptop. Download this *OpenPlotter Settings* package: |Latest version of 'openplotter-settings' @ Cloudsmith| and follow the :ref:`Desktop and laptop<getting_started_installing_desktop>` chapter to install OpenPlotter from scratch.

.. |Latest version of 'openplotter-settings' @ Cloudsmith| image:: https://api-prd.cloudsmith.io/v1/badges/version/openplotter/openplotter/deb/openplotter-settings/latest/a=all;d=debian%252Fbullseye;t=binary/?render=true&show_latest=true
   :target: https://cloudsmith.io/~openplotter/repos/openplotter/packages/detail/deb/openplotter-settings/latest/a=all;d=debian%252Fbullseye;t=binary/


OpenPlotter Expert
******************

Pi-gen is the tool used to create the official *Raspberry Pi OS* images. We use a fork of pi-gen to create OpenPlotter images. Use the *openplotter32* and *openplotter64* branchs of our repository to create your own OpenPlotter flavor. You need good knowledge of Linux to create your own OpenPlotter distributions. Follow instructions in `README file <https://github.com/openplotter/pi-gen/>`_.
