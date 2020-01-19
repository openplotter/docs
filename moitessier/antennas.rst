Antennas
########

.. tip::
	For the best receiving performance, ensure that the cable lengths  of the antennas are as short as possible.

.. caution::
	It is recommended to use pigtail adapters to reduce mechanical force on the antenna connectors.

	.. image:: img/antennas1.png
			:align: center

AIS Antenna
***********

The Moitessier HAT supports all popular VHF/AIS antennas. Please note the following features when selecting an antenna:

- 50 Ohm impedance
- SMA male connector for direct connection, or any other connector using a proper pigtail adapter
- Frequency range at least 161.95 MHz to 162.05 MHz
- RG 174 coaxial cable or better

.. caution::
	The coaxial cable attached to the SMA connector should have a maximum outside diameter of 3.7 mm. Larger diameters might cause mechanical force to the antenna connector.

A suitable splitter also enables the Moitessier HAT to share the VHF antenna of other radio equipmenton a ship. 

.. danger::
	Use splitters only that physically decouple the Moitessier HAT from any transmitter while transmission is in progress.

GNSS Antenna
************

Your device has an internal patch antenna. If it is not possible to  fit the HAT with an unobstructed view of the sky (such as below deck), an external GNSS antenna is required. Use a standard, active GNSS antenna that is fitted with a BNC connector.
 