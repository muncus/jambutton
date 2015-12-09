# Jam-O-Matic

Based on [github.com/garthvh/esp8266button](https://github.com/garthvh/esp8266button).

This version of the ESP8266 IoT button is designed to run on battery for a long
time. Rather than rely on the ESP8266 sleep mode, it uses a logic-level
P-channel mosfet circuit to control power to the ESP chip. In the inactive
state, the power draw is extremely low. When the button is pressed, the esp8266
chip wakes up, triggers the IFTTT event, and then powers itself off (by sending
voltage to the P-fet's gate).

After designing the P-channel mosfet control, I realized that Adafruit's
[pushbutton power switch](https://www.adafruit.com/products/1400) is exactly
what I had in mind, so i went with one of those instead. Pick up a [micro-lipo
charger](https://www.adafruit.com/products/1904) and you've got all the
necessary materials.

> TODO: circuit diagram.

![button guts](http://marcdougherty.com/images/jamomatic-guts.jpg)

see [github.com/garthvh/esp8266button](https://github.com/garthvh/esp8266button) for original docs.
