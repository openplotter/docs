.. _downloading:

Downloading
###########

.. important::
    The latest models of Raspberry 4 with the latest firmware will not boot with these OpenPlotter 2 images of the **Basic** method. If this is your case, you have to use the **Advanced** method until we finish OpenPlotter 3.

+--------------+------------------------------------+-----------------------------------------------------------------------------------------------------+
| Level        | Platform                           | Download                                                                                            |
+==============+====================================+=====================================================================================================+
| **Basic**    | - Raspberry Pi 3                   | - :download:`OpenPlotter Starting <https://cloud.openmarine.net/s/sL9doDML7P4CQDo>`                 |
|              | - Raspberry Pi 4 **\***            | - :download:`OpenPlotter Headless <https://cloud.openmarine.net/s/Yapesa2XPJptgaz>`                 |
|              |                                    | - :download:`OpenPlotter Moitessier HAT <https://cloud.openmarine.net/s/mgakCZ5BSJYsysa>`           |
|              |                                    | - OpenPlotter À la Carte (under construction)                                                       |
+--------------+------------------------------------+-----------------------------------------------------------------------------------------------------+
| **Advanced** | - Raspberry Pi 3                   | :download:`OpenPlotter Settings deb <https://github.com/openplotter/openplotter-settings/releases>` |
|              | - Raspberry Pi 4 **\***            |                                                                                                     |
|              | - Debian derivative 32-bit         |                                                                                                     |
|              | - Debian derivative 64-bit **\***  |                                                                                                     |
+--------------+------------------------------------+-----------------------------------------------------------------------------------------------------+
| **Expert**   | - Raspberry Pi 3                   | :download:`OpenPlotter pi-gen <https://github.com/openplotter/pi-gen/tree/openplotter>`             |
|              | - Raspberry Pi 4 **\***            |                                                                                                     |
+--------------+------------------------------------+-----------------------------------------------------------------------------------------------------+

**\*** Recommended

.. admonition:: What to choose?

    Some OpenPlotter features are exclusive for Raspberry Pi but if you do not need them you can install OpenPlotter in any computer running a Linux Debian derivative like *Ubuntu*, *Linux Mint* or even *Raspberry PI OS*. That is the first question you should ask yourself.

    We try to provide solutions for everyone, from newbies to experts. The second question would be, *what do I know about Linux?* or even, *I am a Linux expert but I feel lazy, should I choose a ready-to-use option?* The text below will help you answer these questions.

Basic
*****

This is the easiest and fastest way of having OpenPlotter working. Our OpenPlotter distributions are based on Rasbian. We publish different editions according to the most demanded uses containing all the required apps installed and preconfigured. Just plug and sail!

**OpenPlotter Starting** - All required apps to fulfill most OpenPlotter marine features.

:Installed apps: Settings, OpenCPN installer, Signal K installer, Xygrib, Network, Dashboards, Serial, CAN, Docs 

**OpenPlotter Headless** - *Starting* edition apps ready to be used remotely without monitor.

:Installed apps: *Starting* edition.
:Settings: WiFi access point enabled, ssh enabled, remote desktop enabled.

**OpenPlotter Moitessier HAT** - *Starting* edition apps plus required apps to use the Moitessier HAT out of the box.

:Installed apps: *Starting* edition, I2C, Pypilot.
:Settings: GNSS reception, AIS reception, compass, hell, pitch, pressure.

**OpenPlotter À la Carte** (under construction) - *Starting* edition apps plus any app of your election. You will be able to customize some settings too.

:Installed apps:
:Customizable settings:

You do not need previous knowledge of Linux to install and use these OpenPlotter distributions. Follow the :ref:`basic manual<getting_started_installing>` to install them on your SD card.

Advanced
********

.. important::
    OpenPlotter 2 only works in Debian 10 buster 32-bit. You need to download and install Raspberry Pi OS (Legacy) from the offcial site: https://www.raspberrypi.com/software/operating-systems

    We are already working on OpenPlotter 3 for Debian 11 bullseye 32-bit and 64-bit, but it is still in beta and not recommended for production. Go here to test and help with development: https://forum.openmarine.net/showthread.php?tid=3878

You can install OpenPlotter from scratch in any computer running your favourite Debian derivative distribution, and of course in *Raspberry PI OS*. Hovewer, if your distribution is not *Raspberry PI OS* and your computer is not a Raspberry Pi, you will not be able to install some apps. 

:Common apps: Settings, Docs, OpenCPN installer, Xygrib, Signal K installer, Dashboards, Network, Serial, CAN, IoT, Signal K filter, Kplex, SDR VHF
:Raspberry apps: Pypilot, Moitessier HAT, I2C sensors, GPIO

You need basic knowledge of Linux to install OpenPlotter from scratch. Follow the :ref:`advanced manual<getting_started_installing>` to install OpenPlotter from scratch.

Expert
******

Pi-gen is the tool used to create the official *Raspberry PI OS* images. We use a fork of pi-gen to create OpenPlotter images. Use the *openplotter* branch of our repository to create your own OpenPlotter flavor.

You need good knowledge of Linux to create your own OpenPlotter distributions. Follow instructions in `README file <https://github.com/openplotter/pi-gen/blob/openplotter/README.md>`_.
