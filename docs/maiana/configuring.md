# Configuring OpenPlotter

You can configure OpenPlotter to get AIS and GNSS data from a MAIANA transponder with just a few clicks. You will also learn how to enable transmission, configure the device, and update the firmware.

## Getting AIS and GNSS data

MAIANA is ready to rceive and send AIS and GNSS data out of the box, just power on the device and connect by USB or UART to OpenPlotter. We want to send MAIANA data to the Signal K server so that any program like OpenCPN can access AIS and GNSS data. We will do it easily using the ![Serial](img/usb.png) *Serial* app.

!!! note
	If connected via USB, skip the UART steps.

If you are connected by UART, first of all you need to enable the UART interface of your Raspberry Pi. Click ![UART](img/uart.png) ``UART0`` and then click ``Yes``. Remember that enabling the UART0 interface will disable Bluetooth if you are in Raspberry Pi 3 or 4. You can use any of the UART interfaces that you have [available on your Raspberry Pi](../serial/serial_app.md#uart) by connecting to the appropriate pins.

![uart0](img/uart0.png)

Acknowledge the warning, and reboot the Raspberry Pi:

![uart1](img/uart1.png)  
*Raspberry Pi model 3 and 4*

![uart2](img/uart2.png)  
*Raspberry Pi model 5*

After enabling UART or just plugging in the USB and clicking ![refresh](img/refresh.png) ``Refresh``, you will see a new device listed. Select this new device and provide a short name for the *alias* and select `NMEA 0183` under *data*. If it is connected by USB check *Remember device* and if it is connected by UART check *Remember port*. Click ![apply](img/apply.png) ``Apply`` when done.

![maiana2](img/maiana2.png)

Go to the ![connections](img/connections.png) *Connections* tab and select the new device you just created. Click ![sk](img/sk.png) ``Add to Signal K`` and then click ``AUTO``. A connection will be created on the Signal K server for your device.

![maiana3](img/maiana3.png)

![maiana4](img/maiana4.png)

Make sure there is an OpenCPN enabled [connection to the Signal K server](../opencpn/skconnection.md) and your are done.

![opencpnAIS](../opencpn/img/opencpnAIS.jpg)

## Connecting to MAIANA

Using the ![maiana](img/maiana.png) *MAIANA AIS transponder* app you can manage all the settings of your device. Open the ![Settings](../settings/img/openplotter-settings.png) *Settings* app, select this app and click ![install](img/install.png) `Install`.

![maiana5](img/maiana5.png)

Open the ![maiana](img/maiana.png)*MAIANA AIS transponder* app and select the connection we previously configured with the ![usb](img/usb.png) *Serial* app by clicking on the ``MAIANA Signal K connection`` field:

![maiana6](img/maiana6.png)

And that's it. All connections have been made and you will be able to communicate with MAIANA every time you open the ![maiana](img/maiana.png) *MAIANA AIS transponder* app and the device is turned on. If you can not get a connection the first time, try again by clicking ![refresh](img/refresh.png) ``Refresh``.

![maiana7](img/maiana7.png)

## Enabling transmission

If we want to enable transmission, we must provide the station data. Complete the form using this syntax for each field:

- ***MMSI***: you should have one for your boat already.
- ***Vessel name***: up to 20 alphanumeric characters, no punctuation. Use all caps.
- ***Call sign***: may be empty if you do not have one.
- ***Vessel type***: this is the numeric type of the vessel, see below.
- ***LOA***: length in meters (integer only).
- ***Beam***: width in meters (integer only).
- ***Port Offset***: meters from the port side where the unit is located.
- ***Bow Offset***: meters from the bow where the unit is located.

For vessel type, here are some numeric values that apply to class B transponders:

- 30 - Fishing
- 34 - Diving
- 36 - Sailing
- 37 - Pleasure craft

Click ![apply](img/apply.png) ``Save station data`` when you are done:

![maiana8](img/maiana8.png)

You will see that the value of *Station data* has changed to *provided* in green:

![maiana9](img/maiana9.png)

There are 2 switches to turn on/off transmission:

- **Hardware**: There is a physical switch on all the adapters. The breakout board also has a pin for this. This switch has priority over the Software switch.

- **Software**: You will find a button *Software TX switch* in ![maiana](img/maiana.png) *MAIANA AIS transponder* app.

This is the relation between the two states of these switches:


| Hardware | Software | TX  |
|----------|----------|-----|
| ON       | ON       | ON  |
| ON       | OFF      | OFF |
| OFF      | X        | OFF |

Turn on your hardware switch, click ![refresh](img/refresh.png) ``Refresh`` and you will see that the value of *Hardware TX switch* has changed to *ON* in green:

![maiana10](img/maiana10.png)

Now click ![switch-on](img/switch-on.png) ``Software TX switch`` and you will see that the value of *Software TX switch* has changed to *ON* in green and the value of *Status* has changed to *transmitting* in green:

![maiana11](img/maiana11.png)

Congratulations, you are already transmitting!

## Notifications actions

If you have the ![notifications](img/notifications.png) *Notifications* app installed, you will see two new actions added to the list to automatically turn the software TX switch on and off upon receiving a specific notification:

![noti1](img/noti1.png)

![noti2](img/noti2.png)

## Detecting EMI

MAIANA constantly checks for noise floor on both channels to detect any electromagnetic interference (EMI) near your device. If you enable ![notifications](img/notifications.png) ``Detect noise`` and the noise level is higher than 64, an alert notification will be sent to the Signal K server.

![maiana12](img/maiana12.png)

If you have the ![notifications](img/notifications.png)*Notifications* app installed, you will see an alert window like this one:

![maiana12a](img/maiana12a.png)

## Updating firmware

You will receive your MAIANA base kit with the latest stable firmware installed. Go to the ![install](img/install.png) *Firmware* tab and click ![refresh](img/refresh.png) ``Refresh`` to see the version of your device:

![maiana13](img/maiana13.png)

Click ![update](img/update.png) ``Download Firmware`` to find the bin file that corresponds to your MCU and hardware revision from the project page:

![maiana14](img/maiana14.png)

Ignore the last digit of your hardware revision -- it does not matter. So if you have board 11.3.0 with an STM32L422 processor, the right binary is maiana-stm32l422-hw11.3-fwXXX.bin where XXX is the latest revision you see here. If you already have this firmware on your board, there is no update:

![maiana14a](img/maiana14a.png)

Once the correct file is downloaded click ![file](img/file.png)``Update firmware`` to start the firmware update process:

![maiana15](img/maiana15.png)

Select the file, click ``Open`` and finally ``Yes``:

![maiana15a](img/maiana15a.png)

![maiana15b](img/maiana15b.png)

The system will stop the Signal K server to make sure it can take control of the device and load the new firmware. When done, both the Signal K server and the device will reboot:

![maiana16](img/maiana16.png)
