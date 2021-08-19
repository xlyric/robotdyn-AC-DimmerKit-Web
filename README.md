# # DIY IoT AC-Dimmer KIT, ESP8266 Wi-Fi D1 Mini for AC 110~240V dimming control.

This is a WORKING exemple of application with the AC-Dimmer KIT from Robotdyn... 
https://robotdyn.com/diy-iot-ac-dimmer-kit-esp8266-wi-fi-d1-mini-for-ac-110-240v-dimming-control.html

![enter image description here](https://robotdyn.com/pub/media/catalog/product/cache/3c7e6817bfdaeedae5fc1f56c1800828/i/o/iotdimmer_angle2_esp_logo.jpg)


# Installation

make a git clone of the project and use Visual studio code for build and upload to the board. 
I made test with D5 and D6 but by default, D0 and D1 is used and solt on the board. 

# USE

at the first start, the wemos use the Wifimanager for configure the Wifi. 

```mermaid
sequenceDiagram
Start -->> New Wifi : 
New Wifi -->> Configure: 192.198.4.1
Configure -->> Start : wifi configured 
Start  -->> Run : Open Website and Dim
```

# CHANGE POWER
for change power use the web site : 
Control :  http://IP/?POWER=xx
xx max = 99 

```mermaid
sequenceDiagram
Website -->> Dimmer : ?POWER=x
Dimmer -->> Website : Apply
```
# note on Robotdyn librairie
with actual version of arduino GUI or VS, the librairie not working
I modify the librairie and is called in the lib_deps variable
lib_deps = https://github.com/xlyric/RBDDimmer

