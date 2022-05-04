# ESP32WebControllerPrometheus
Includes Webserver, to control the state of an IO-pin. Also includes endpoint, which can be fetched with prometheus.

# Usage
1. Upload sketch to ESP32 board
2. Connect a common button to PIN32 (With pull-down resistor, so by default button state is LOW, until its pressed)
3. To establish the first connection, press button to set ESP32 in Hotspot Setup mode
4. Search with your smartphone (or other wifi device) for wifi-network "ESP32-AP" - connect to it
5. A popup should get opened and you see the configuration UI - click "Configure Wifi Network" and select your local wifi, store credentials
6. After 60 seconds, the device will try to connect to the given network credentials which you´ve entered
7. Finally, open the Webserver by enter the IP-address into your browser. There you can switch the IO Pin-2, which will trigger the internal blue ESP32 LED to ON/OFF
8. You can use the endpoint /state behind the IP-address, to open the prometheus endpoint- there you can see the state of the IO-Pin, which can be crawled by your own prometheus server to collect metrics.