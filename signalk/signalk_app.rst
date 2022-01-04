.. |OPsignalk| image:: img/openplotter-signalk-installer.png

|OPsignalk| Signal K Installer
##############################

.. note::
	To run this app type this in a terminal:

	.. parsed-literal::

		openplotter-signalk-installer

.. image:: img/signalk1.png

.. |OPsignalkReinstall| image:: img/reinstall.png
.. |OPsignalkSettings| image:: img/settings2.png
.. |mhelp| image:: ../img/help.png
.. |mSettings| image:: ../img/settings.png

|mhelp| ``Help`` opens an offline copy of this documentation in a browser and |mSettings| ``Settings`` opens the main app *OpenPlotter Settings*.

|OPsignalkReinstall| Reinstall Signal K
***************************************

After installing this *OpenPlotter Signal K Installer* app, the Signal K server should be also installed and you do not have to do anything else to start using it. We add this option in case you need to reinstall the server from scratch if it ever becomes unstable. 

.. caution::
	Reinstalling the signal K server will remove the current plugins, login credentials and settings.

|OPsignalkSettings| Settings
****************************
.. |OPsignalkApply| image:: img/apply.png
.. |OPsignalkCancel| image:: img/cancel.png
.. |OPsignalkVessel| image:: img/ship.png

*OpenPlotter Signal K Installer* app installs the server using port 3000 by default. To access the web administration panel of the Signal K server, you can use this URL from the browser included in OpenPlotter:

.. parsed-literal::

	http://localhost:3000

Or this one from a browser running on any computer connected to the same network:

.. parsed-literal::

	http://openplotter.local:3000

Using port 80, the URLs would be:

.. parsed-literal::

	http://localhost
	http://openplotter.local

You can change the port or enable SSL at any time without losing your current settings. Use |OPsignalkApply| ``Apply`` to save changes or |OPsignalkCancel| ``Cancel`` to reload current settings.

Click |OPsignalkVessel| ``Vessel Data`` to set some important data of your boat like name, MMSI, call sign, draft ... You need to login to access this section of the web administration panel.

Logging in
##########

.. image:: img/signalk2.png

.. image:: img/signalk3.png

**Signal K Security**

When you enter the Signal K admin ui, it will ask you for a name and a password to create an administrator account.
Once you do that you will be offered the login page.

The last menu item in the ui is security. You can add/delete users and change passwords ...

**If you have lost the password**

You can reset Signal K security by:

1) Open a terminal
2) Delete the existing file: /home/pi/.signalk/defaults.json
3) Run the setup sudo signalk-server-setup. Accept the update option rather than configuring from scratch. Select no for port 80 and SSL
4) Navigate to the login page with a browser. Note that the option is now not to login but instead to create an administrator account. Once you do that you will be offered the login page.

More info
#########

how does it work
SK manuals

plugins