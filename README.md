# Sonoff Dual R2 Modified

A person send to me a sonoff dual R2 to revive. After he flash tasmota in it, he lost some IDs necessary to restore the original 
sonoff firmware. So, how i can fix it?. 

First, the microcontroller of the sonoff basic R2 is the ESP8266. Also, i need the "new" smart switch works just
like the original, with the same functions, that remote operation is possible and that it can be connected to google home, alexa or something similar.

After some research, i found [SinricPro](https://sinric.pro/es-index.html). They solve this problems, and give you 3 devices for free. 
[Here](https://github.com/sinricpro/esp8266-esp32-sdk) you can find some examples and other info.

## Flashing Sonoff Dual R2
Serial interface is available at the bottom left end of the sonoff dual PCB in the image below(header J2). Also, you can see the connection 
between the sonoff and the FTDI. Is necessary connect GPIO0(BUTTON 0) and GND during power up to put the chip in programming mode (in header J1).

![image](https://user-images.githubusercontent.com/101881891/220759075-04a9e3ae-8d54-416e-90d9-ca45114dfb69.png)

## Use external switches

The relays can be controlled by external push buttons or switches connected to the header J1. This add a manual control.
BUTTON 0 (on GPIO0) connected to GND controls Relay1 and BUTTON 1 (on GPIO9) connected to GND controls Relay2.
