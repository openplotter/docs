# Connecting a USB GPS receiver


To see how this all works, we are going to configure the most basic device, a USB GPS receiver. In ![Devices](img/openplotter-serial.png) ``Devices`` tab, select the device and enter a name for it in the ``alias`` field. Select the type of ``data`` that flows through the device (NMEA 0183 in this case) and finally select whether the system should ``remember the device`` or the position of the USB port where the device is plugged in.

![gps1](img/gps1.png)

Press ![Apply](img/apply.png) ``Apply`` when done and the device will be marked green:

![gps2](img/gps2.png)

Unplug the device and press ![Refresh](img/refresh.png) ``Refresh`` to check if the system detects the lost device:

![gps3](img/gps3.png)

Plug the device back in, press ![Refresh](img/refresh.png) ``Refresh`` and you are ready to configure any program using your device's alias and be sure it will always work. 

To send data from the USB GPS to OpenCPN, you need to first connect the device to the Signal K server and then connect OpenCPN to the Signal K server. In ![Connections](img/connections.png) ``Connections`` tab, select the *ttyOP_gps* device and press ![Add to Signal K](img/sk.png) ``Add to Signal K``:

![gps4](img/gps4.png)

!!! note
	Select ![Add to GPSD](img/gpsd.png) ``Add to GPSD`` only if you want GPSD to manage your GPS/AIS device. All GPSD and Signal K settings will be created automatically.

!!! note
	Select ![Add to Pypilot](../pypilot/img/autopilot.png)``Add to Pypilot`` only if you are using a pypilot controller. Pypilot will send data to the Signal K server automatically.

Then select the ``Baud Rate`` required by your device and press ``AUTO``:

![gps5](img/gps5.png)

The signal K server will restart and the connection will be marked green:

![gps6](img/gps6.png)

And you are done. Check in Signal K server the new connection:

![gps7](img/gps7.png)

And check OpenCPN to make sure there is a [connection to the Signal K server](../opencpn/skconnection.md).
