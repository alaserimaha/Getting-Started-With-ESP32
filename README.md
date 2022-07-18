# Getting-Started-With-ESP32
## 1. What is the ESP32 board?
## 2. How to Install the ESP32 board ?
## 3. Virtual example of using the ESP32 board ?
## 4. How to control ESP32 board ?
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

### 3.Plug the ESP32 board to your computer:
With your Arduino IDE open, follow these steps:

    1.
       * Select your Board in Tools > Board menu 
       * Select the Port (if you don’t see the COM Port in your Arduino IDE, you need to install the [CP210x USB to UART Bridge VCP Drivers]()):
         https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
       * Then, click the “OK” button .
    2.
       * Open the Boards Manager. Go to Tools > Board > Boards Manager…
       * Search for ESP32 and press install button for the “ESP32 by Espressif Systems“
       * That’s it. It should be installed after a few seconds.

