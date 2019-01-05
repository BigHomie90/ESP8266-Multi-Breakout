# ESP8266-Multi-Breakout

This is an ESP8266 [NodeMCU V3 LoLin](https://www.aliexpress.com/item/New-Wireless-module-NodeMcu-Lua-WIFI-Internet-of-Things-development-board-based-ESP8266-with-pcb-Antenna/32656775273.html) break-out PCB I've created for use with Home Assistant. I created this layout to allow for various functions; a garage door opener or retrofitting to a 'dumb' alarm system to integrate existing PIRs into your smart home setup.

The board will accept a +12VDC, 1A input via a 2.1MM centre positive jack. This voltage is regulated down to +5VDC via the onboard AMS1117-5.0 linear regulator (http://www.advanced-monolithic.com/pdf/ds1117.pdf) to feed power to the two +5V relays and the NodeMCU v3 (LoLin).

The board also accommodates the following sensors:

[**DHT22**](https://www.aliexpress.com/item/DHT22-single-bus-digital-temperature-and-humidity-sensor-module-2302-electronic-building-blocks/32753887461.html) - Temperature and Humidity sensor

[**HC-SR04**](https://www.aliexpress.com/item/1pcs-HC-SR04-to-world-Ultrasonic-Wave-Detector-Ranging-Module-for-arduino-Distance-Sensor/32786781050.html) - Ultrasonic distance sensor

Aside from the above, a LM339N (http://www.ti.com/lit/ds/symlink/lm339.pdf) is also available onboard and powered by the +12VDC input. This can be used to integrated to your existing alarm system to make use of the PIRs as binary sensors for motion detection. See here for more info (https://www.instructables.com/id/Alarm-PIR-Movement-to-Home-Automation/).

Pin out as follows:

| Pin  | Function |
| ------------- | ------------- |
| D0  | N/A  |
| D1  | DHT22  |
| D2  | Free  |
| D3  | Free  |
| D4  | Free  |
| D5  | HC-SR04 (Trig)  |
| D6  | HC-SR04 (Echo)  |
| D7  | Relay #1  |
| D8  | Relay #2  |

See here for [pin reference](https://github.com/thehookup/Wireless_MQTT_Doorbell/blob/master/GPIO_Limitations_ESP8266_NodeMCU.jpg). 

Integration to Home Assistant can be done using the [esphomeyaml library](https://esphomelib.com/esphomeyaml/index.html).
