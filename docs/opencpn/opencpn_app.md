# OpenCPN Installer

Install this app from the ![Settings](../settings/img/openplotter-settings.png) *Settings* app and open it by clicking ![OpenCPN Installer](img/opencpn-installer.png) `OpenCPN Installer` under `Main -> OpenPlotter` or typing this in a terminal:

```console
openplotter-opencpn-installer
```

![OpenCPN1](img/opencpn1.png)

![Help](../settings/img/help.png) ``Help`` opens an offline copy of this documentation in a browser and ![Settings](../settings/img/openplotter-settings.png) ``Settings`` opens the main app.

OpenCPN can be installed on multiple Debian derivatives (Raspberry OS, Ubuntu, Mint...) and these OS can be installed on multiple architectures (i386, armhf, arm64, amd64...). We have added all the ways to install OpenCPN to ![OpenCPN Installer](img/opencpn-installer.png) *OpenCPN Installer* app so you can choose the one that best suits your system.

## ![](img/check.png) Check Versions

When you open the app, all buttons are disabled. You have to check the current versions present in all the installed sources. This could take even a minute the first time.

A list will be displayed with the different versions of all the available sources and some recommendations:

![OpenCPN2](img/opencpn2.png)

You can install OpenCPN in two different ways, from the **Debian/Ubuntu** repositories or from **Flatpak**. You can use both ways and install two instances of OpenCPN that can be used simultaneously on the same machine without problems. 

In Flatpak there is only one source and therefore only one version but in Debian/Ubuntu there are several sources and several versions available:

- **Debian/Ubuntu**: This is the official Debian/Ubuntu repository. There is an OpenCPN package, but it will probably always be old.

- **Ubuntu PPA**: This is an special repository to be added in Ubuntu but it will also work in Debian and Raspberry OS. Packages in this repository are always up to date and are fully compatible with packages in the official Debian/Ubuntu repositories above.

- **Debian/Ubuntu Backports**: The official backports repositories are used to install packages that exist in higher versions of the system that have not yet been updated in the current system version.

## Which source to choose?

After checking the versions, the buttons on the ![Install](img/opencpn24.png)``Install`` tab will be enabled:

![OpenCPN3](img/opencpn3.png)

- ![](img/debian.png) **Debian/Ubuntu - Ubuntu PPA**: This option will install the highest version found in the official *Debian/Ubuntu* repository or the *Ubuntu PPA* repository.

- ![](img/debian.png) **Debian/Ubuntu Backports**: This option will install the latest version in the official *Debian/Ubuntu Backports* repository.

- ![](img/flatpak.png) **Flatpak**: This option will install the latest version in the *Flatpak* repository. This option runs OpenCPN in a kind of container independent of the host system and for this reason the time and size of the download will be larger. 

!!! note
	As a general rule, you should always choose the highest version, regardless of the source, unless you need to use an OpenCPN plugin that is not included or does not work in higher versions.


	If the sources *Debian/Ubuntu - Ubuntu PPA* and *Debian/Ubuntu Backports* contain the same version, choose *Debian/Ubuntu Backports*.


	The Debian/Ubuntu repositories only release OpenCPN packages for LTS (Long-Term Support) versions of your operating system. If you use a development version of Debian or Ubuntu you should use OpenCPN Flatpak.


	At the time of writing this manual, OpenCPN Flatpak may not work well in headless and touchscreen environments.

Sometimes when we install a new version, some plugins may not be compatible and cause OpenCPN to crash or prevent it from opening. If this happens we can try to remove the old plugins by deleting the *~/.local/lib/opencpn* folder and reinstalling the plugins when OpenCPN opens normally again.

If you install OpenCPN twice, from Debian/Ubuntu and Flatpak, the system will differentiate between them by adding the FP suffix to the version installed from Flatpak:

![OpenCPN4](img/opencpn4.png)

## OpenCPN Installer actions

Once OpenCPN is installed, there are a few actions you can take in this app. 

- You can ![Uninstall](img/uninstall.png) ``Uninstall`` OpenCPN at any time.

- By checking ![Autostart](img/autostart.png) ``Autostart``, OpenCPN will run automatically at startup and by checking ![Full Screen](img/fullscreen.png)  ``Full Screen``, it will use the entire screen.

- By clicking ![Open](img/open.png) ``Open``, OpenCPN will run.
