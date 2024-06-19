# Input data by slcand

This tutorial is for any NMEA 2000 converter that can connect via USB using *slcand* such as the devices available from [CANable](https://canable.io/).

First of all you have to define the device using the ![Serial](../serial/img/openplotter-serial.png) *Serial* app. Then return to this ![Canb Bus](img/can.png) *CAN Bus* app and click ![Add device](../serial/img/openplotter-serial.png) ``Add device`` in the ![slcand](../serial/img/openplotter-serial.png)  ``slcand`` tab:

![canSlcand1](img/canSlcand1.png)

Select the device you defined in the ![Serial](../serial/img/openplotter-serial.png) *Serial* app and click ``OK``:

![canSlcand2](img/canSlcand2.png)

From this moment you should receive data on your device. Select the item from the list and click ![check](img/check.png) ``Check device traffic`` to confirm data entry:

![canSlcand3](img/canSlcand3.png)

![canSlcand4](img/canSlcand4.png)

Now we need to get this data to the Signal K server. Select the connection from the list and click ![sk](img/sk.png) ``Add Connection``. The Signal K server will restart and you are done:

![canSlcand5](img/canSlcand5.png)

![canSlcand6](img/canSlcand6.png)

Go to the Signal K server administration interface to confirm that the connection is now active:

![canSlcand7](img/canSlcand7.png)

Check OpenCPN to make sure there is a [connection to the Signal K server](../opencpn/skconnection.md) and you are getting data from your NMEA 2000 network.
