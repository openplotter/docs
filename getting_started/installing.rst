.. _getting_started_installing:

Installing
##########

Basic
*****

This is the easier and most common way to have OpenPlotter working on a Raspberry Pi in few minutes. You only need a micro SD card (minimum 8GB, recommended 16GB) and a computer with an SD card reader.

- Download and unzip your preferred OpenPlotter edition from the **Basic** section in :ref:`downloading<downloading>` chapter.

- Download and install :download:`Raspberry Pi Imager <https://www.raspberrypi.org/software/>`. 

- Put the SD card you will use with your Raspberry Pi into the reader and run *Raspberry Pi Imager*.

- Click on ``CHOOSE OS`` and then on ``Use custom``:

.. image:: img/imager.png

- Select the .img file of your preferred OpenPlotter edition.

- Click on ``CHOOSE SD CARD`` and select your SD card.

- Click on ``WRITE`` and take a coffe.

- Remove the SD card from the reader, insert it into the raspberry and you are done.

After the first boot you can customize and localize your system changing some important settings like password or system language. You can also change these settings later in :menuselection:`Main --> Preferences --> Raspberry Pi configuration`.

.. danger::
	You MUST change the default password for the user *pi*. Otherwise, any user will be able to access your system easily.

If you are using the **OpenPlotter Headless** edition, you should see the SSID of the access point after a few seconds of inserting the SD into the Raspberry and turning it on.

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

To Install OpenPlotter on any computer running a Linux Debian derivative system (*Raspberry PI OS*, *Ubuntu*, *Linux Mint*...) you have to install the dependencies.

Open a terminal and type:

.. parsed-literal::

	sudo apt update
	sudo apt install python-configparser python3-wxgtk4.0 python3-ujson python3-pyudev whois vlc

Now you have to install the main app ``openplotter-setting`` from the .deb file you can download from the *Advanced* section in :ref:`downloading<downloading>` chapter.

After downloading the .deb file, you can install it by double click or typing this in a terminal:

.. parsed-literal::

	sudo dpkg -i openplotter-settings_x.x.x-stable.deb

Every time OpenPlotter needs to perform an action that requires administrator permission, it will ask for the password. To avoid having to continuously enter your administrator password you can add your user to the *sudoers* list. Do this only if you know what you are doing:

.. parsed-literal::

	sudo visudo

Add this line to the end of the document and save:

.. parsed-literal::

	myuser ALL=(ALL) NOPASSWD: ALL
