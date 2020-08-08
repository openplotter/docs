Configuration
#############

.. sidebar:: OpenPlotter Moitessier HAT edition

   `Download <https://nx8035.your-storageshare.de/s/mgakCZ5BSJYsysa>`_ the img or NOOBS file and follow the :ref:`basic manual<getting_started_installing>` to install it on your SD card.

The easiest way to make Moitessier HAT work on Raspberry Pi is to download and install a special OpenPlotter edition. Everything is preinstalled and preconfigured in *OpenPlotter Moitessier HAT* edition and it will work out of the box, just plug and sail!

It is recommended to read the rest of the chapter to learn how to configure the HAT on your own and be able to play with its settings.

.. important::
	If you are using the *OpenPlotter Moitessier HAT* edition, the only thing you should do is calibrate the compass following the steps of the :ref:`Pypilot compass calibration<calibration>` chapter.

	You should reinstall the driver at least once even if everything works fine to make sure that your HAT firmware is up to date, especially Moitessier HAT 1 users.

If you are not using the *OpenPlotter Moitessier HAT* edition, you have to be sure the list of apps below are installed. These apps have to be installed from ``OpenPlotter Settings`` interface.

- ``OpenCPN Installer``
- ``Signal K Installer``
- ``Serial``
- ``Pypilot``
- ``Moitessier HAT``
- ``I2C``

.. image:: img/system0.png

After installing these apps go to ``Moitessier HAT`` app and click on ``Check System``:

.. image:: img/system1.png

You could see some error messages because SPI and I2C interfaces are disabled or the Moitessier HAT driver is not installed yet:

.. image:: img/system2.png

SPI and I2C must be enabled before installing the drivers. Go to applications menu and enable both of them in :menuselection:`Preferences --> Raspberry Pi configuration --> Interfaces`:

.. image:: img/system3.png

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

.. image:: img/gps2.png

Configuring AIS and GNSS reception
**********************************

Go to ``Serial`` app and select the HAT from the the list of detected devices in ``Devices`` tab. Provide a short ``alias`` and select NMEA 0183 as the format of the expected ``data``. Finally click ``Apply``:

.. image:: img/gps3.png

Go to ``Connections`` tab, select the HAT from the list, click on ``Add to Signal K`` and in the next window click ``AUTO``. This way we are creating a serial connection in ``Signal K`` server using the settings provided by ``Serial`` app.

.. image:: img/gps4.png

.. image:: img/gps4bis.png

.. note::
	If you are going to use an autopilot you should select ``Add to Pypilot`` and finally connect pypilot to ``Signal K``. See :ref:`pypilot<pypilot>` chapter for details.

Go to ``Info`` tab and click on ``Check configuration`` again to see the changes:

.. image:: img/gps4bis2.png

Configuring compass, heel and trim reception
********************************************

Go to ``Pypilot`` app an select ``Only compass``.

.. note::
	If you are going to use an autopilot you should select ``Autopilot``. See :ref:`pypilot <pypilot>` chapter for details.

.. image:: img/compass2.png

Then go to ``connections``, select the available connection and click on ``Add connection``. This way we are creating a network connection in ``Signal K`` to receive heading, pitch and heel data.

.. image:: img/compass3.png

.. important::
	To get reliable heading readings you have to calibrate the compass following the steps of the :ref:`Pypilot compass calibration<calibration>` chapter.

Go to ``Info`` tab and click on ``Check configuration`` again to see the changes:

.. image:: img/compass4.png

Configuring pressure reception
******************************

Go to ``Sensors`` tab in ``I2C`` app an click ``Add``.

.. image:: img/pressure2.png

Select ``MS5607-02BA03`` in the list of detected sensors and click ``OK``.

.. image:: img/pressure3.png

A Signal K key will be created for pressure by default. You can assign another one for temperature. The temperature sensor is affected by the heat produced by the Raspberry and the HAT itself, so we can not assign this value to environment.inside.temperature key, we should use something like environment.openplotter.temperature. Select ``temperature`` and click in ``Edit``.

.. image:: img/pressure4.png

To choose a Signal K key click ``Edit``.

.. image:: img/pressure5.png

Select ``environment`` in the first column and ``inside.*.temperature`` in the second column. Write *openplotter* in the ``Replace`` field, press ``Replace`` button and the wildcard will be replaced by *openplotter*. Press ``OK``.

.. image:: img/pressure6.png

We do not need pressure or temperature data every second so we will select another ``Rate``. Click ``OK``. Edit the ``pressure`` value to select another ``Rate`` too.

.. image:: img/pressure7.png

Go to ``Connections`` tab, select ``MS5607-02BA03`` sensor and click in either ``Add Connection`` to create a new network connection in ``Signal K`` or ``Edit port`` if you want to send these data to any existing network connection in ``Signal K``.

.. image:: img/pressure8.png

Go to ``Info`` tab and click on ``Check configuration`` again to see the changes:

.. image:: img/pressure9.png

Configuring OpenCPN
*******************

As of version 5.2, OpenCPN can manage Signal K data, so we no longer need to convert Signal K data to NMEA 0183. You just need to create this connection in OpenCPN:

.. image:: img/opencpn1.png

The default port of the Signal K server is 3000, but you can change it. If you are not sure which port you have configured, go to the ``Signal K Installer`` app to check.

.. figure:: img/compass6.png

	Magnetic Heading (circle), Course Over Ground (square)

.. figure:: img/pressure10.png

	Heel, Pitch and Pressure

.. figure:: img/gps5.jpg

	AIS

Go to ``Info`` tab and click on ``Check configuration`` again to see the changes:

.. image:: img/opencpn2.png
