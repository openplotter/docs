# Downloading

!!! note "Raspberry Pi or desktop/laptop computer?"

	OpenPlotter is optimized to be used on [Raspberry Pi](https://www.raspberrypi.com) computers, but you can also install OpenPlotter on any desktop or laptop computer running Linux Debian or any derivative like Ubuntu, Mint ... Some OpenPlotter apps that are used to manage some sensors connected via GPIO will not be available when installed on desktop and laptop computers. See a list [here](downloading.md#desktop-and-laptop).

## Raspberry Pi images

This is the easiest and fastest way to get started with OpenPlotter. We publish different editions according to the most demanded uses that contain all the required apps installed and preconfigured. We try to provide solutions for everyone from beginners to experts. We even have a fully customizable option that will save you a lot of time. Just plug and sail!

Our OpenPlotter editions are based on Raspberry Pi OS. You do not need any prior knowledge of Linux to install and use them. Follow the [installing](installing.md) chapter to learn how.

### OpenPlotter Starting

All required apps to fulfill most OpenPlotter marine features.

- **Download**: [OpenPlotter Starting](https://cloud.openmarine.net/s/TwxS4AJrtTJ485T)
- **Hostname**: openplotter
- **User**: pi
- **Password**: raspberry
- **Language**: en_GB.UTF-8
- **Keymap**: gb
- **Layout**: English (UK)
- **TimeZone**: Europe/London
- **Wi-Fi client**: SSID: none, Password: none, Country: none
- **Wi-Fi AP**: SSID: none, Password: none, IP: none
- **SSH**: Disabled
- **Remote desktop**: Disabled
- **Touchscreen**: Disabled
- **Backlight**: Disabled
- **Installed apps**: Settings - Docs - Signal K installer - OpenCPN installer - Serial - CAN bus - Dashboards - Notifications - Xygrib

### OpenPlotter Headless

Same as *OpenPlotter Starting* but ready to be used remotely without monitor. The Raspberry Pi's internal Wi-Fi device is configured in dual mode, this means that there is a preconfigured access point but it can also connect as a client.

- **Download**: [OpenPlotter Headless](https://cloud.openmarine.net/s/cMJrfH45aPeamFc)
- **Hostname**: openplotter
- **User**: pi
- **Password**: raspberry
- **Language**: en_GB.UTF-8
- **Keymap**: gb
- **Layout**: English (UK)
- **TimeZone**: Europe/London
- **Wi-Fi client**: SSID: none, Password: none, Country: none
- **Wi-Fi AP**: SSID: openplotter, Password: 12345678, IP: 10.42.0.1
- **SSH**: Enabled
- **Remote desktop**: Enabled
- **Touchscreen**: Disabled
- **Backlight**: Disabled
- **Installed apps**: Settings - Docs - Signal K installer - OpenCPN installer - Serial - CAN bus - Dashboards - Notifications - Xygrib

### OpenPlotter Touchscreen

Same as *OpenPlotter Starting* but ready to be used on DSI touchscreens as the official monitor for Raspberry Pi and its clones.

- **Download**: [OpenPlotter Touchscreen](https://cloud.openmarine.net/s/3gjyKsrpKRb6ZHe)
- **Hostname**: openplotter
- **User**: pi
- **Password**: raspberry
- **Language**: en_GB.UTF-8
- **Keymap**: gb
- **Layout**: English (UK)
- **TimeZone**: Europe/London
- **Wi-Fi client**: SSID: none, Password: none, Country: none
- **Wi-Fi AP**: SSID: none, Password: none, IP: none
- **SSH**: Disabled
- **Remote desktop**: Disabled
- **Touchscreen**: Enabled
- **Backlight**: Enabled
- **Installed apps**: Settings - Docs - Signal K installer - OpenCPN installer - Serial - CAN bus - Dashboards - Notifications - Xygrib

### OpenPlotter À la Carte

Fill in a form with all the available customization options and in a few minutes you will receive an image built by a robot from scratch and to your liking that will save you a lot of time. Another advantage over the other editions is that all packages that make up the OS, including Openplotter apps, will be updated to the latest versions.

- **Download**: Coming soon.
- **Hostname**: Customizable
- **User**: Customizable
- **Password**: Customizable
- **Language**: Customizable
- **Keymap**: Customizable
- **Layout**: Customizable
- **TimeZone**: Customizable
- **Wi-Fi client**: SSID: Customizable, Password: Customizable, Country: Customizable
- **Wi-Fi AP**: SSID: Customizable, Password: Customizable, IP: Customizable
- **SSH**: Customizable
- **Remote desktop**: Customizable
- **Touchscreen**: Customizable
- **Backlight**: Customizable
- **Installed apps**: Customizable

## Desktop and laptop

!!! important
	Each new version of OpenPlotter should only be installed on the indicated system. **OpenPlotter v4 will work only on Debian 12 Bookworm, Ubuntu 22.04 Jammy or any of their derivatives**. If you try to force an installation of OpenPlotter v4 over OpenPlotter v3 (based on Debian 11 Bullseye), your system will become unstable.

You can also install OpenPlotter in any desktop or laptop computer running your favourite Debian derivative distribution. Hovewer, if your computer is not a Raspberry Pi, you will not be able to install some OpenPlotter apps:

- **Common**: Settings - Docs - Signal K installer - OpenCPN installer - Serial - CAN bus - Dashboards - Notifications - IoB - MAIANA AIS Transponder - Xygrib - AvNav installer - SDR VHF

- **Only Raspberry Pi**: Pypilot - I2C Sensors - GPIO

You just need basic knowledge of Linux to install OpenPlotter for desktop and laptop. Download this *OpenPlotter Settings* package: [![Latest version of 'openplotter-settings' @ Cloudsmith](https://api-prd.cloudsmith.io/v1/badges/version/openplotter/openplotter/deb/openplotter-settings/latest/a=all;xc=main;d=debian%252Fbookworm;t=binary/?render=true&show_latest=true)](https://cloudsmith.io/~openplotter/repos/openplotter/packages/detail/deb/openplotter-settings/latest/a=all;xc=main;d=debian%252Fbookworm;t=binary/) and follow the [Desktop and laptop](installing.md#desktop-and-laptop) chapter to install OpenPlotter from scratch.

## OpenPlotter Expert

Pi-gen is the tool used to create the official *Raspberry Pi OS* images. We use a fork of pi-gen to create OpenPlotter images. Use the *openplotter64* branch of our repository to create your own OpenPlotter flavor. You need good knowledge of Linux to create your own OpenPlotter distributions. Follow instructions in [README file](https://github.com/openplotter/pi-gen/tree/openplotter64).
