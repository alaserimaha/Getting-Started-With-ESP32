# Getting-Started-With-ESP32
## 1. What is the ESP32 board?
## 2. How to Install the ESP32 board ?
## 3. Plug the ESP32 board to your computer .
## 4. Virtual example of using the ESP32 board .
![ESP32](https://user-images.githubusercontent.com/60073836/179428836-b86665c8-d158-4bd0-a64d-ffbbd3b28245.png)

## 1. What is the ESP32 board?
ESP32 is the name of the chip that was developed by Espressif Systems. 
ESP32 can perform as a complete standalone system . 
And it can interface with other systems to provide Wi-Fi and Bluetooth functionality through its SPI / SDIO or I2C / UART interfaces.

For more information about the widget and its uses [click here ](https://www.nabto.com/guide-to-iot-esp-32/)

## 2. How to Install the ESP32 board ?
The Arduino IDE allows you to program ESP32 functionality using the Arduino IDE and its programming language on your own device and any operating system.

Here are some steps that enable you to connect the ESP32 with the Arduino IDE:


<img src="https://user-images.githubusercontent.com/60073836/179429357-10386d91-48c4-4f53-a921-6b14d936301c.png" width=25% height=25%>


### 1: Install Arduino IDE:
[From the Arduino website](https://www.arduino.cc/en/software) install the Arduino IDE
Make sure to download the latest version .

### 2: Add ESP32 on Arduino IDE:
To install the ESP32 board in your Arduino IDE, follow these next instructions:
     
     
    1.
       * In your Arduino IDE, go to File> Preferences
       * Enter the following into the “Additional Board Manager URLs” field: 
         https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
       * Then, click the “OK” button .
    2.
       * Open the Boards Manager. Go to Tools > Board > Boards Manager…
       * Search for ESP32 and press install button for the “ESP32 by Espressif Systems“
       * That’s it. It should be installed after a few seconds.

### 3. Plug the ESP32 board to your computer:
With your Arduino IDE open, follow these steps:

    
       - Select your Board in Tools > Board menu 
       - Select the Port (if you don’t see the COM Port in your Arduino IDE, you need to install the CP210x USB to UART Bridge VCP Drivers)):
       - Open the following example under File > Examples > WiFi (ESP32) > WiFiScan
       - A new sketch opens in your Arduino IDE
       - Press the Upload button in the Arduino IDE. Wait a few seconds while the code compiles and uploads to your board.
       - If everything went as expected, you should see a “Done uploading.” message.
       - Open the Arduino IDE Serial Monitor at a baud rate of 115200
       - Press the ESP32 on-board Enable button and you should see the networks available near your ESP32
       
## 4. Virtual example of using the ESP32 board .
There are several sites that allow you to interact with an ESP32  Virtualy
It will be very useful to practice before starting
Like [wokwi simulator ]( https://wokwi.com/projects/new/esp32)
You will see the ESP32 piece on the right and the sketch to write the code on the left

<img src="https://user-images.githubusercontent.com/60073836/179430696-f03b9a65-e10f-46b4-b9de-59c3200d252c.png" width=50% height=50%>

Now, this is an example of writing a code that turns on traffic lights

First, let's explain the program:
In this project we will create a traffic light controlled by the ESP32 card where the Red led lights up for 3 seconds, then goes out and the Green led    lights up for 3 seconds and then goes out so that the orange led lights up for 1 second. Then the program starts over and starts over.



When starting with the tools, you will need:
   - ESP32
   - Green LED
   - Yellow LED
   - Red LED
   - 3 resistors of 220Ω
   - Connecting wires

<img src="https://user-images.githubusercontent.com/60073836/179430838-d3797522-35d0-4a7f-b380-06bac284cdd9.png" width=50% height=50%>

Then we start mounting
To perform the assembly, you can connect :
the yellow LED resistor to pin D23, 
the green LED resistor to pin D22 ,
and the red LED resistor to pin D21 of the ESP32 board.

<img src="https://user-images.githubusercontent.com/60073836/179430924-bf3dc10c-ad3a-41b6-99bd-7d0ad5dfdb8e.png" width=50% height=50%>

Then we go to write the code in the sketch section :

Here is the traffic light schedule:

    import time
    from machine import Pin
    led_jaune=Pin(23,Pin.OUT) #Sets ESP32 board pin D23 to output mode
    led_rouge=Pin(22,Pin.OUT) # Sets ESP32 board pin D22 to output mode
    led_verte=Pin(21,Pin.OUT) # Sets ESP32 board pin D21 to output mode

    while True:
       led_jaune.value(1) #Turn on yellow LED
       led_rouge.value(0)
       led_verte.value(0)
       time.sleep(1) # wait 1s
       led_jaune.value(0) 
       led_rouge.value(1) #Turn on red LED
       led_verte.value(0) 
       time.sleep(3)
       led_jaune.value(0) 
       led_rouge.value(0)
       led_verte.value(1) #Turn on green LED
       time.sleep(3)

### Run, and here we have a mini traffic light.


### The reference:
- https://randomnerdtutorials.com/installing-the-esp32-board-in-arduino-ide-windows-instructions/
- https://www.nabto.com/guide-to-iot-esp-32/
- https://www.robotique.tech/robotics/traffic-light-with-esp32/
