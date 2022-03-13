.. |mhelp| image:: ../img/help.png
.. |mSettings| image:: ../img/settings.png
.. |OPavnav| image:: img/sailboat48rinstall.png
.. |OPavnavStop| image:: img/stop.png
.. |OPavnavStart| image:: img/start.png
.. |OPavnavRestart| image:: img/restart.png
.. |OPavnavSettings| image:: img/settings2.png
.. |OPavnavRun| image:: img/sailboat24r.png
.. |OPavnavRun2| image:: img/sailboat24rs.png

|OPavnav| AvNav Installer
#########################


.. note::
	To run this app type this in a terminal:

	.. parsed-literal::

		openplotter-avnav

.. image:: img/avnav0.png

|mhelp| ``Help`` opens an offline copy of this documentation in a browser and |mSettings| ``Settings`` opens the main app *OpenPlotter Settings*.


This app installs AvNav, a web chart plotter, on OpenPlotter based systems. It also offers some additional settings, so no changes in the ~/avnav/data/avnav_server.xml file are needed:

- Enable/Disable ``Autostart`` of the AvNav server.
- |OPavnavStop| ``Stop``, |OPavnavStart| ``Start`` and |OPavnavRestart| ``Restart`` the AvNav server.
- Change ports in |OPavnavSettings| ``Settings`` to avoid conflicts with other apps.
- Open the browser running |OPavnavRun| a single instance or split the window to run |OPavnavRun2| 2 instances of AvNav.

By default, AvNav listens on port 8080. It is the same as opening the Signal K administration UI in the browser, the only difference is that Signal K listens on port 3000 instead of 8080.

.. note::
	Read `here <http://wellenvogel.de/software/avnav/docs/beschreibung.html?lang=en>`_  the full documentation.

 