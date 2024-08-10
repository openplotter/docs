# Examples of actions

## ![](img/op.png) Engage pypilot using a GPIO button

You can use a momentary switch and connect it as shown in the image below:

![actions-pypilot-1](img/actions-pypilot-1.png)

For this example it is necessary to have the ![](img/autopilot.png) Pypilot, ![](img/gpio.png) *GPIO* and ![](img/notifications.png) *Notifications* apps installed and updated to their latest versions.

Once the switch is wired, open the ![](img/gpio.png) *GPIO* app and in the ![](img/digital.png) `Digital` tab click on ![](img/gpio.png) `Add input`.

![actions-pypilot-2](img/actions-pypilot-2.png)

In the next window, fill in the fields as shown in the image below. Make sure that the *Send initial state* option is not checked, as we do not want the autopilot to engage when turning on the system in case the switch has been accidentally closed. We do not need to set up any visual method for the notification, but perhaps it would be nice to have an audio:

![actions-pypilot-3](img/actions-pypilot-3.png)

Finally open the ![](img/notifications.png) *Notifications* app and in the ![](img/op.png) Actions tab click ![](img/add.png) Add:

![actions-pypilot-4](img/actions-pypilot-4.png)

In the next window fill in the fields as shown in the image below, press `OK` and you are done!

![actions-pypilot-5](img/actions-pypilot-5.png)

![actions-pypilot-6](img/actions-pypilot-6.png)

By pressing the momentary switch you will be able to verify that the autopilot is engaged in the pypilot *Web interface* because the AP icon moves to the right and turns green as shown in the image below:

![Web Interface](../pypilot/img/soft-web.png)

To disengage the autopilot, you can use another momentary switch and repeat the process, but this time using another GPIO, for example GPIO8, and selecting `Pypilot: disengage AP` in the *Actions* field instead of `Pypilot: engage AP`.


You can also use a two-state switch (on/off) and use only one GPIO, but it could be confusing if when you turn off the system the switch is on and when you turn on the system the autopilot is not engaged. Enabling *Send initial state* would cause the autopilot to engage in this case, but could create dangerous situations.