# ESP32-CAM-DS18B20--Soil-thermometer
-> Quickly assembled thermometer from basic parts I had at home without use. I ended up using these parts as a thermometer in the attic when I needed to measure the temperature 
   to see if I could work in the attic. temperature data are sent to a channel on the thingspeak platform.


-> HOW TO PROGRAM ESP32-CAM
To program the ESP32-CAM you need to use an Arduino Uno desk and cables to connect it as you can see it at picture 
![image](https://github.com/DominikTomasek/ESP32-CAM-DS18B20--Soil-thermometer/assets/55549002/660c1d7a-0435-4a78-8d69-0c33d8c69a58)
The wiring of the Arduino UnO and ESP32 - CAM is as follows, first thing we need to connect the 5 V power supply and GND, this is explained by the red and black lines in the picture, red for 5 V and black for GND.  The second thing is to connect the UART communication between ESP32 - CAM and Arduino Uno, we achieve this by connecting the TX pin of Arduino Uno and UoT to ESP32 - CAM for sending data and for receiving data we put a connection between RX pin of Arduino and UoR to ESP32 - CAM for receiving data. The third step is to connect the RESET and GND pins on the Arduino and on the ESP32-CAM. If these steps are completed, the code from the computer will start to be uploaded to the ESP32-CAM. One should keep in mind that sometimes it is necessary to press the reset button on the bottom of the board to start recording. This problem could be solved by connecting a 10 µF capacitor to the ENABLE pin, but this pin is not shown on this model of microcontroller.

-> WIRE CONNECTIONS BETWEEN ESP32-CAM AND OTHERS PARTS:
![image](https://github.com/DominikTomasek/ESP32-CAM-DS18B20--Soil-thermometer/assets/55549002/fc1a4b0c-7fc8-4bbc-81e9-e0854fb92263)

DS18B20 wire connections:
![image](https://github.com/DominikTomasek/ESP32-CAM-DS18B20--Soil-thermometer/assets/55549002/43f22e73-4a1d-4c7a-8541-307bdcf95479) ![image](https://github.com/DominikTomasek/ESP32-CAM-DS18B20--Soil-thermometer/assets/55549002/61f8be7d-7842-4590-891d-d15e26b37f79)

![image](https://github.com/DominikTomasek/ESP32-CAM-DS18B20--Soil-thermometer/assets/55549002/eb0f4f17-4eeb-436c-9773-cb220823616c)


-> HOW TO STAR A DAVICE:

1. Connect the power supply to the ESP32-cam itself , because the DS18B20 thermometer and the led must be disconnected during startup , this is probably due to the large current draw during WiFi startup.
   
2. Wait a while before the device connects to WiFi for about 10s to 20s, then connect the LED to pin GPIO 13, if the LED lights up the device is connected and the LED signals that it is connected to WiFi and sends temperature data to Thingspeak.
   
3.As the last one connect thermometer DS18B20 to pins GND, 5V and GPIO 13 then after a while the temperature on the channel on Thingspeak platform will show 


->USED COMPONENTS: 
1. ESP32-CAM desk
2. DS18B20
3. Yellow led diode
4. 4K7 Ohm resistor
5. 270 Ohm resistor 
6. UTP cable
7. Female pin conectors
8. Female cable conector for power supply
9. Wiring box
10. AC/DC adapter 12V / 0,5A

Device final form:
![image](https://github.com/DominikTomasek/ESP32-CAM-DS18B20--Soil-thermometer/assets/55549002/e0df92ab-f6b7-4e6f-b42b-e0bb42b87da7)

SOURCE:
[1] https://randomnerdtutorials.com/esp32-ds18b20-temperature-arduino-ide/

[2] https://randomnerdtutorials.com/esp8266-nodemcu-thingspeak-publish-arduino/

[3] https://www.analog.com/media/en/technical-documentation/data-sheets/ds18b20.pdf

