.. |OPSDRico| image:: img/sdr.png
.. |OPSDRedit| image:: img/edit.png
.. |OPSDRproc| image:: img/process.png
.. |OPSDRstart| image:: img/start.png

AIS
###

*AIS* tool comes pre-installed in |OPSDRico| *SDR VHF*. To start receiving AIS data you just have to follow a few simple steps.

Select *AIS* app and click on |OPSDRedit| ``Edit``:

.. image:: img/ais1.png

Select the device you want to use to get AIS data from the *Detected SDR devices* list.

You can set the receive *Gain*. Not always the maximum gain will work better, we recommend leaving this field blank for auto.

Set the *PPM* value for your device. If you have calibrated your device, you should see this value in the device list. You can also set any value to test.

Provide a *Port* to send AIS data (default 10110). A UDP network connection will be created in Signal K automatically for that port.

.. image:: img/ais2.png

Click on ``Save``.

.. image:: img/ais3.png

Go to the |OPSDRproc| *Processes* tab and check ``Autostart`` on AIS process to start getting data at system startup:

.. image:: img/ais4.png

Finally, select the AIS process and click |OPSDRstart| ``Start`` to start getting data:

.. image:: img/ais5.png

If you see the AIS process in green, you are done:

.. image:: img/ais6.png

To confirm that everything is working fine, go to the Signal K server and check if an *OpenPlotter SDR AIS* connection has been created and is getting data:

.. image:: img/ais7.png

Then, go to OpenCPN and confirm that a connection with the Signal K server exists and is getting AIS data:

.. image:: ../img/opencpnConnection.png
.. image:: img/ais9.jpg


Antennas
********

Each tool included in |OPSDRico| *SDR VHF* uses a specific frequency range and you will need a specific antenna for each of them.

AIS signals are broadcast at both 161.975 MHz and 162.025 MHz and have a maximum range of approximately 75 kilometers. So if you are more than 75 kilometers away from any boats, you will probably not be able to receive AIS signals. AIS is also considered a line of sight signal, meaning that if there are large buildings or mountains in the way of your antenna and the boats, AIS signals could be blocked. Because of this reason it is important to put your antenna as high up as possible.
There are multiple commercial AIS or VHF antennas designed for marine use that will work. However, sometimes `home made antennas <https://www.sailworldcruising.com/news/227075/Build-your-own-inexpensive-VHF-AIS-antenna>`_ work even better and they of course are cheaper.
