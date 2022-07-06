.. _dAISy:

.. |OPserialUart| image:: img/uart.png
.. |OPserialUSB| image:: img/usb.png
.. |OPserialApply| image:: img/apply.png
.. |OPserialConnections| image:: img/connections.png
.. |OPserialSK| image:: img/sk.png

Connecting the dAISy HAT
########################

.. image:: img/daisyHat1.png

**Specification**

* True two channel receiver, continuously receiving on AIS channels A (161.975 MHz) and B (162.025 MHz)
* Superior sensitivity compared to other low-cost AIS receivers
* Low power, less than 200mW in receive mode (<40mA at 5V)
* 38400 baud serial output in industry standard NMEA format (AIVDM)
* Communicates with Raspberry Pi via UART0 (serial0)
* Works with Raspberry Pi 1 (A+/B+ only), Pi 2, Pi 3, Pi 4 and Pi Zero
* Shape and size compliant with Raspberry Pi HAT standard
* Breakout pads for 2 independent TTL serial outputs, 3.3 and 5 volt rails, and Raspberry Pi I2C port
* SMA antenna connector
* SMA-to-BNC adapter and hex standoffs included

.. note::
	This product is available in the `OpenMarine Shop <http://shop.openmarine.net/>`_. Buying at OpenMarine Shop helps us keep the project alive.

	On the `original product page <https://shop.wegmatt.com/products/daisy-hat-ais-receiver>`_ you will find the full specification and a better choice for US buyers.

**Configuration**

Mount the dAISy HAT in your Raspberry Pi and enable a serial port in the GPIO header of the Raspberry Pi by clicking the |OPserialUart| ``UART0`` icon:

.. image:: img/daisyHat2.png

Acknowledge the warning, and reboot the Raspberry Pi:

.. image:: img/daisyHat3.png

After the reboot, launch the *OpenPlotter Serial app* again. On the |OPserialUSB| *Devices* tab, you should now see a new entry. Select the line with *ttyAMA0*, give it an alias (for example daisy) and select 
*NMEA 0183* from the data dropdown, then press |OPserialApply| ``Apply``:

.. image:: img/daisyHat4.png

Now we need to connect the *ttyOP_daisy* device to the Signal K server, the central data processing hub of OpenPlotter. Switch to the |OPserialConnections| *Connections* tab, select the *ttyOP_daisy* device and click |OPserialSK| ``Add to Signal K``:

.. image:: img/daisyHat6.png

From the *Baud Rate* dropdown menu select *38400*, then press ``AUTO``:

.. image:: img/daisyHat7.png


You are done, the Signal K server and any program connected to it, such as OpenCPN, should now receive AIS data. Check OpenCPN to make sure there is a connection to the Signal K server and that it is getting data from your DAISy HAT:

.. image:: ../img/opencpnConnection.png

.. image:: img/opencpnAIS.jpg