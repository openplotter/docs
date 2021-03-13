I2C
###
Go into >Openplotter>Settings and then hit refresh.

In the list of openplotter Apps, go down to I2C Sensors and select then install.

Now go to >Preferences>Rasp Pi Config and go to the interfaces tab, enable I2C.

Powerdown the Pi and install the sensor(s)

I2C uses several pins - pins1 (3.3V), 3(SDA), 5(SCL), 9(GND).  Connect them up accordingly based on your devices.

Power the Pi back up

Got to >Openplotter>I2C and add all sensors providing a name for each that makes sense and fits with the Signal K specification, see http://signalk.org/specification/1.0.4/doc/signalk.pdf, see the picture below:

.. image:: img/i2c1.png

On the connection Tab, add connection to Signal K for each of the sensors:

.. image:: img/i2c2.png

*the Pypilot entry will not show up until you have done the Pypilot configs
