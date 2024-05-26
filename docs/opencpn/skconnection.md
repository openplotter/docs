# Signal K connection

To receive data from all your devices and sensors on OpenCPN, the recommended way is to create all connections on the Signa K server and then create a single connection to the server on OpenCPN using these settings:

- **Type**: Network

- **Protocol**: Signal K

- **Address**: localhost

- **DataPort**: 3000 (or the custom port you have set in the ![Signal K Installer](../signalk/img/skinstaller.png) *Signal K installer* app)

 - **Uncheck**: Automatic server dicovery


![SK connection](img/skconnection.png)