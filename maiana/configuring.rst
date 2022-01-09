Configuring OpenPlotter
#######################

You can configure OpenPlotter to get AIS and GNSS data from a MAIANA transponder with just a few clicks. You will also learn how to enable transmission, configure the device, and update the firmware.

Getting AIS and GNSS data
*************************

MAIANA is ready to rceive and send AIS and GNSS data out of the box, just power on the device and connect by USB or UART to OpenPlotter. We want to send MAIANA data to the Signal K server so that any program like OpenCPN can access AIS and GNSS data. We will do it easily using the *OpenPlotter Serial* app.


If you are connected by UART, first of all you need to enable the UART interface of your Raspberry Pi. Click ``UART`` and then click ``Yes``. Remember that enabling the UART interface will disable Bluetooth. If you are connected by USB, skip this step.

.. image:: img/maiana8.png
.. image:: img/maiana9.png

After enabling UART or just plugging in the USB and clicking ``Refresh``, you will see a new device listed. Select this new device and provide a short name for the *alias* and select NMEA 0183 under *data*. If it is connected by USB check *Remember device* and if it is connected by UART check *Remember port*. Click ``Apply`` when done.

.. image:: img/maiana10.png
.. image:: img/maiana11.png

Go to the *Connections* tab and select the new device you just created. Click ``Add to Signal K`` and then click ``AUTO``. A connection will be created on the Signal K server for your device.

.. image:: img/maiana12.png
.. image:: img/maiana13.png
.. image:: img/maiana14.png

Make sure there is an OpenCPN enabled connection to the Signal K server and your are done.

.. image:: img/maiana15.png
.. image:: img/maiana16.jpg

Connecting to MAIANA
********************

Using the *OpenPlotter MAIANA AIS transponder* app you can manage all the settings of your device. Open *OpenPlotter Settings* app, select this app and click ``Install``.

.. image:: img/maiana17.png

Under construction

.. image:: img/maiana18.png
.. image:: img/maiana19.png
.. image:: img/maiana20.png
.. image:: img/maiana21.png
.. image:: img/maiana22.png
.. image:: img/maiana23.png

Enabling transmission
*********************

Under construction

.. image:: img/maiana24.png
.. image:: img/maiana25.png
.. image:: img/maiana26.png
.. image:: img/maiana27.png

Detecting EMI
*************

Under construction

.. image:: img/maiana28.png
.. image:: img/maiana29.png

Updating firmware
*****************

Under construction

.. image:: img/maiana30.png
.. image:: img/maiana31.png
.. image:: img/maiana32.png
.. image:: img/maiana33.png
