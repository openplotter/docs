.. _getting_started_installing:

Installing
##########

Basic
*****

This is the easier and most common way to have OpenPlotter working on a Raspberry Pi in few minutes. Download your preferred OpenPlotter edition from the *Basic* section in :ref:`downloading<downloading>` chapter.

.. note::
	You will find each OpenPlotter edition in two formats, *img* and *New Out Of Box Software* (NOOBS). Contents of both img and NOOBS formats are identical, the only difference is the way to install OpenPlotter in your SD-card. 

	When using NOOBS files, a recovering partition will be created in the SD and you will be able to re-install OpenPlotter from it. 

	When using img files, this partition is not created and you can use all the SD space for the system. 

	Since SD cards corruption occurs more frequently than desired, we recommend NOOBS because the recovery partition is never mounted and will never be corrupted so it will always be available for :ref:`recovery<recovery>`.

You have to follow the official Raspberry manual to install a img/NOOBS file in your SD but using our img/NOOBS file instead the Raspberry file.

- `Installing image files <https://www.raspberrypi.org/documentation/installation/installing-images/README.md>`_
- `Installing NOOBS files <https://www.raspberrypi.org/documentation/installation/noobs.md>`_

After the first boot you can customize and localize your system changing some important settings like password or system language in :menuselection:`Preferences --> Raspberry Pi configuration`.

.. danger::
	You must change the default password for the user *pi*. Otherwise, any user will be able to access your system easily.

Most of these settings an more can be configured before building the system if you use the **OpenPlotter À la Carte** edition.

If you are using the img option of the **OpenPlotter Headless** edition, you should see the SSID of the access point after a few seconds of inserting the SD into the Raspberry and turning it on.

If you are using the NOOBS option, to see the SSID of the access point you should wait for the system to be installed about 30 minutes the first time. The next boots, the SSID will be visible after a few seconds of turning it on.

These are the access data to connect remotely to OpenPlotter when you use this headless edition:

+--------------------+-------------------------------------+
| **Access Point**   | :SSID: openplotter                  |
|                    | :Password: 12345678                 |
+--------------------+-------------------------------------+
| **IP**             | :IP: 10.10.10.1                     |
|                    | :Address: openplotter.local         |
+--------------------+-------------------------------------+
| **SSH**            | :Command: ssh pi\@openplotter.local |
|                    | :Password: raspberry                |
+--------------------+-------------------------------------+
| **Remote desktop** | :Address: openplotter.local         |
|                    | :Port: 5900                         |
|                    | :User: pi                           |
|                    | :Password: raspberry                |
+--------------------+-------------------------------------+

.. danger::
	You must change the default access point password in ``OpenPlotter Network`` app. Otherwise, any user will be able to access your system easily.


Advanced
********

To Install OpenPlotter on any computer running a Linux Debian derivative system (Raspbian, Ubuntu, Mint...) you have to install the dependencies.

Open a terminal and type:

.. parsed-literal::

	sudo apt update
	sudo apt install python-configparser python3-wxgtk4.0 python3-ujson python3-pyudev whois vlc

Now you have to install the main app ``openplotter-setting`` from the .deb file you can download from the *Advanced* section in :ref:`downloading<downloading>` chapter.

After downloading the .deb file, you can install it by double click or typing this in a terminal:

.. parsed-literal::

	sudo dpkg -i openplotter-settings_x.x.x-stable.deb

OpenPlotter apps will appear under *Others* category in the main menu of your system. If you create the category *OpenPlotter*, all openplotter apps will appear under that category. 
