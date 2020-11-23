.. _downloading:

Downloading
###########

+--------------+------------------------------------+-----------------------------------------------------------------------------------------------------+
| Level        | Platform                           | Download                                                                                            |
+==============+====================================+=====================================================================================================+
| **Basic**    | - Raspberry Pi 3                   | - :download:`OpenPlotter Starting <https://nx8035.your-storageshare.de/s/sL9doDML7P4CQDo>`          |
|              | - Raspberry Pi 4 **\***            | - :download:`OpenPlotter Headless <https://nx8035.your-storageshare.de/s/Yapesa2XPJptgaz>`          |
|              |                                    | - :download:`OpenPlotter Moitessier HAT <https://nx8035.your-storageshare.de/s/mgakCZ5BSJYsysa>`    |
|              |                                    | - OpenPlotter À la Carte                                                                            |
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

    Some OpenPlotter features are exclusive for Raspberry Pi but if you do not need them you can install OpenPlotter in any computer running a Linux Debian derivative like Ubuntu, Mint or even Raspbian. That is the first question you should ask yourself.

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

You can install OpenPlotter from scratch in any computer running your favourite Debian derivative distribution, and of course in Raspbian. Hovewer, if your distribution is not Raspbian and your computer is not a Raspberry Pi, you will not be able to install some apps. 

:Common apps: Settings, Docs, OpenCPN installer, Xygrib, Signal K installer, Dashboards, Network, Serial, CAN, IoT, Signal K filter, Kplex, SDR VHF
:Raspberry apps: Pypilot, Moitessier HAT, I2C sensors, GPIO

You need basic knowledge of Linux to install OpenPlotter from scratch. Follow the :ref:`advanced manual<getting_started_installing>` to install OpenPlotter from scratch.

Expert
******

Pi-gen is the tool used to create the raspberrypi.org Raspbian images. We use a fork of pi-gen to create OpenPlotter images. Use the *openplotter* branch of our repository to create your own OpenPlotter flavor.

You need good knowledge of Linux to create your own OpenPlotter distributions. Follow instructions in `README file <https://github.com/openplotter/pi-gen/blob/openplotter/README.md>`_.
