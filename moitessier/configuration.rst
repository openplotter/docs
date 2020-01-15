Configuration
#############

.. sidebar:: OpenPlotter Moitessier HAT edition

   `Download <https://nx8035.your-storageshare.de/s/mgakCZ5BSJYsysa>`_ the img or NOOBS file and follow the :ref:`manual to install<getting_started_installing>` it on your SD card.

The easiest way to make Moitessier HAT work on Raspberry Pi is to download and install a special OpenPlotter edition. Everything is preinstalled and preconfigured in *OpenPlotter Moitessier HAT* edition and it will work out of the box, just plug and sail!

However, you should read the rest of this section to learn how to configure the HAT on your own and be able to play with its settings.

If you are not using the *OpenPlotter Moitessier HAT* edition you should install these OpenPlotter apps from ``OpenPlotter Settings`` app in your system in order to configure and use your Moitessier HAT:

- ``OpenCPN Installer``
- ``Signal K Installer``
- ``Serial``
- ``Pypilot``
- ``Moitessier HAT``
- ``I2C``

After installing these apps go to ``Moitessier HAT`` app and click on ``Check System``:

.. image:: img/system1.png

You could see some error messages because SPI and I2C interfaces are disabled or the Moitessier HAT driver is not installed yet:

.. image:: img/system2.png

SPI and I2C must be enabled before installing the drivers. Go to applications menu and enable both of them in ``Preferences -> Raspberry Pi configuration -> Interfaces``:

.. image:: img/system3.png

.. warning::
	If you disable SPI after installing the driver or you manage to install it before enabling SPI, your system could hang when you try to enable SPI again. If this happens, uninstall the package, reboot and try again.

Installing drivers
******************

The driver must match your kernel version. After updating your system, the kernel could be also updated and your HAT will stop working. In ``Drivers`` tab you will find your current kernel version. Select the package matching your kernel and click on ``Install``. The drivers will be installed and the system rebooted. The package may need to do this twice, you will be notified.

.. image:: img/system4.png

After rebooting you should see a list of kernels supported by the installed driver. If your current kernel is not supported by any of the available packages, click on ``Download`` and the system will try to find a suitable package from Internet. If this fails too, click on ``All drivers`` to go to *Rooco* site and ask them when the package will be available.

.. image:: img/system5.png

If everything went well, you should see something like this by clicking on ``Check System`` again:

.. image:: img/system6.png

Now you are ready to configure your system. Go to ``Info`` tab and click on ``Check configuration``. The goal is to send all data to the ``Signal K`` server to be shared with any program that need data from our HAT like OpenCPN. The rest of apps will help us to do this.

.. image:: img/gps1.png

Configuring AIS and GNSS reception
**********************************

.. image:: img/gps2.png

Go to ``Serial`` app and select the HAT from the the list of detected devices in ``Devices`` tab. Provide a short ``alias`` and select NMEA 0183 as the format of the expected ``data``. Finally click ``Apply``:

.. image:: img/gps3.png

Go to ``Connections`` tab, select the HAT from the list, click on ``Add to Signal K`` and in the next window click ``AUTO``. This way we are creating a serial connection in ``Signal K`` server using the settings provided by ``Serial`` app.

.. image:: img/gps4.png

.. note::
	If you are going to use an autopilot you should select ``Add to Pypilot`` and finally connect pypilot to ``Signal K``. See :ref:`pypilot chapter<pypilot>` for details.

When the serial connection with our HAT has been created, ``Signal K`` will send the received NMEA 0183 data to any program connected to the network connection below.

+------------+------------+-----------+
|  Protocol  |   Address  |   Port    |
+============+============+===========+
|    TCP     |  localhost |   10110   |
+------------+------------+-----------+

Be sure this connection exists in OpenCPN and you are done. You should get position and AIS targets:

.. image:: img/gps5.jpg

Configuring compass, heel and trim reception
********************************************

.. image:: img/compass1.png

Configuring pressure reception
******************************

