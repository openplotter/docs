.. _settings:

.. |opsettings| image:: img/openplotter-settings.png

|opsettings| OpenPlotter Settings
#################################

.. note::
	To run this app type this in a terminal:

	.. parsed-literal::

		openplotter-settings

This is the main OpenPlotter app. You need it to install the rest of the apps. If you are using any of the OpenPlotter images for Raspberry Pi, the sources for the repositories where the OpenPlotter apps live will be installed and working, but if you are installing OpenPlotter from scratch you will see something like this:

.. image:: img/settings1.png

.. |appssources| image:: img/sources.png
.. |appcandidates| image:: img/update.png
.. |mout| image:: img/output.png

To install the sources, click |appssources| ``Add sources`` and then click |appcandidates| ``Get Candidates``. You will see the result of each process in the |mout| output tab. After adding the sources you are ready to install the rest of the apps:

.. image:: img/settings2.png

.. |mhelp| image:: ../img/help.png
.. |mautostart| image:: img/autostart.png
.. |mcheck| image:: img/check.png

|mhelp| Help
************

This button will be disabled until you install the *Documentation* app. After installation, the button will be enabled and clicking on it will open an offline copy of this documentation in a browser.

|mautostart| Autostart
**********************

This button should always be checked. Allows self-diagnosis at startup of all OpenPlotter apps and some important settings. It will also trigger some programs and tools configured to run at startup.

|mcheck| Check System
*********************

By clicking this button, you can run the self-diagnosis at any time. Each OpenPlotter app installed will add new processes to diagnose its operation. If something does not work as expected, a red message will show the problem and the solution:

.. image:: img/settings4.png

.. |opapps| image:: img/openplotter-24.png
.. |gsettings| image:: img/debian.png
.. |rsettings| image:: img/rpi.png
.. |slog| image:: img/log.png

|opapps| OpenPlotter Apps
#########################

OpenPlotter apps versions consist of 3 digits separated by periods (a.b.c), a code name and a development state:

:a: This is the OpenPlotter version the app belongs. This value will change only when a new Debian version is released.
:b: This value will change when major updates like new features have been added.
:c: This value will change when minor updates like fixed bugs or translations have been added.
:codeName: Name to identify the OpenPlotter version (a).
:state: **Alpha**: new features need to be added; **Beta**: all features have been added, but need to be tested; **Stable**: all functions should work properly.


.. |apprefresh| image:: img/refresh.png
.. |appinstall| image:: img/install.png
.. |appuninstall| image:: img/uninstall.png
.. |appopen| image:: img/open.png
.. |appchanges| image:: img/changelog.png

|appssources| Add sources
*************************

The sources of the OpenPlotter apps repositories should be added once at the beginning and then only if you see the *missing source* message in any of the OpenPlotter apps.

|appcandidates| Get Candidates
******************************

Occasionally, you should check if there are new versions of OpenPlotter apps in the remote repositories to enjoy new features and correct errors. If there is a new version of an app installed, it will be shown in green:

.. image:: img/settings5.png

|apprefresh| Refresh
********************

Run this option when you want to know the status of your apps. This option only compares versions locally and checks for pending tasks. To compare versions in the remote repositories click |appcandidates| ``Get Candidates``.

|appinstall| Install
********************

To install a new version of any app select the item in the list and click this button. If the updated app was running while the installation, you will have to close and open it again to see changes.

.. image:: img/settings6.png

.. note::
	It is highly recommended to install and update the OpenPlotter apps from *OpenPlotter Settings* because often the installation process involves extra changes to the system that will be carried out automatically. If you install the apps manually from a terminal or they are updated automatically due to a general system update, they will be marked in pink to indicate that there are pending actions:

	.. image:: img/settings7.png

	These extra actions will be executed the first time you open the app:

	.. image:: img/settings8.png

|appuninstall| Uninstall
************************

To uninstall any app select the item in the list and click this button. It is also important to uninstall OpenPlotter apps from *OpenPlotter Settings* to undo the changes in the system.

|appopen| Open
**************

If you have trouble locating and opening the OpenPlotter apps installed on your system, you can open them from here.

|appchanges| Change Log
***********************

Select any app and click this button to see all changes across versions.


|gsettings| General Settings
############################

.. image:: img/settings3.png

.. |GStranslate| image:: img/crowdin.png
.. |GSresize| image:: img/resize.png
.. |GSdelay| image:: img/delay.png
.. |GSplay| image:: img/play.png
.. |GSfile| image:: img/file.png

|GStranslate| Language
**********************

You can select any of the available languages and all OpenPlotter apps will be translated the next time you open them. You can help us with translations by clicking |GStranslate| ``Translate``.

|GSresize| Maximize
*******************

If you enable this option, all OpenPlotter applications will be maximized the next time you open them.

|GSdelay| Delay
***************

Sometimes you may need some devices or programs to be ready before they work normally. Adding seconds to this field and enabling this button will add a delay to the OpenPlotter startup process to allow time for these lazy devices or programs.

|GSplay| Play
*************

You can play a sound to notify you when the OpenPlotter startup process is complete. Select a sound by clicking |GSfile| and enable the |GSplay| ``Play`` button. This is especially useful for headless systems.

|rsettings| Raspberry Settings
##############################

.. image:: img/settings9.png

.. |RSscreensaver| image:: img/screen.png
.. |RSgpio| image:: img/chip.png

|RSscreensaver| Screensaver
***************************

The screensaver is enabled by default in Raspberry OS and this is quite annoying and even dangerous when you are sailing. It is not easy to disable this screensaver and it is not well documented, but using this button you will do it with one click.

|RSgpio| GPIO Map
*****************

Some apps will report which GPIO they are using and you can check it here. Checking a GPIO will return useful information about its usage.

.. image:: img/settings10.png

|slog| System log
#################

.. image:: img/settings11.png

Here are some tools for debugging and troubleshooting your system. When an application malfunctions, it can generate excess messages and eventually create huge log files that consume all free storage space. By setting a maximum log file size, you can detect and resolve potential problems.


.. |SLbug| image:: img/bug.png
.. |SLall| image:: img/logsee.png
.. |SLcat| image:: img/logcategory.png
.. |SLsearch| image:: img/logsearch.png
.. |SLdelete| image:: img/logremove.png

|SLbug| Debugging
*****************

When this button is enabled, OpenPlotter applications will generate error messages that will be saved to the log file or printed on the screen when the application is run from a terminal. Use this feature only to check for errors, do not forget to disable it later because it might slow down performance or lead to oversized log files.

|SLall| See all
***************

This button will print the full contents of the system log file in the |mout| output tab.

|SLcat| See category
********************

Here you can filter the contents of the system log file by some keywords.

|SLsearch| Search
*****************

Here you can filter the contents of the system log file by any term.

|SLdelete| Delete all
*********************

If after debugging the system the log file is too large here you can delete it to start from scratch on the next reboot.
