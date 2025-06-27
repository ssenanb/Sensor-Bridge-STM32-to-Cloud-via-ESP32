# Sensor-Bridge-STM32-to-Cloud-via-ESP32

# Project Description
In this project, embedded systems and IoT architecture are integrated to collect, process and transmit environmental data to a cloud-based platform in real time. The STM32F0 microcontroller collects distance data using an analog IR sensor and temperature and humidity data using a digital DHT11 sensor. This data is transmitted via UART to an ESP32 module. The ESP32 parses the JSON-formatted data and sends it to the ThingSpeak platform via Wi-Fi. In this way, the system demonstrates both intercommunication between embedded units for sensor data processing and IoT-based data transmission to the cloud for visualization via a dashboard.

# Technical Details

-> STM32F0 Side

* Analog data is read via ADC using an IR distance sensor

* Temperature and humidity data is read using the DHT11 sensor

* The data is processed and converted to JSON format

* The JSON data is transmitted to the ESP32 via UART
  
  
-> ESP32 Side

* UART data received from the STM32 is parsed (JSON parsing)

* The data is sent to ThingSpeak via HTTP POST over Wi-Fi
  
-> ThingSpeak Platform

* Data visualizations are provided in graphical or numerical formats

* Data is stored on the Cloud

* Connection is authorized using an API key

# Compenents Used

STM32FODISC

ESP32 WROOM 32D

IR Distance Sensor

DHT11 Temperature and Humidity Sensor

Jumper Cables

Breadboard

Figure 1 : System Overview

<img src="https://github.com/ssenanb/Sensor-Bridge-STM32-to-Cloud-via-ESP32/blob/main/System_Overview1.jpeg" alt="System Overview" width="500"/>

Figure 2 : System Overview 2

<img src="https://github.com/ssenanb/Sensor-Bridge-STM32-to-Cloud-via-ESP32/blob/main/System_Ovreview3.jpeg" alt="System Overview" width="500"/>

Figure 3 : System Overview (the ESP32)

<img src="https://github.com/ssenanb/Sensor-Bridge-STM32-to-Cloud-via-ESP32/blob/main/System_Overview2.jpeg" alt="System Overview" width="500"/>

Figure 4 : Arduino Serial Monitor Output

<img src="https://github.com/ssenanb/Sensor-Bridge-STM32-to-Cloud-via-ESP32/blob/main/Serial_Monitor_Output.png" alt="Output" width="500"/>

Figure 5 : ThingSpeak Output and Dashboard

<img src="https://github.com/ssenanb/Sensor-Bridge-STM32-to-Cloud-via-ESP32/blob/main/ThingSpeak_Output.png" alt="Output" width="500"/>

# Pin Configuration

Figure 6 : Pin Configuration on the STM32CubeIDE

<img src="https://github.com/ssenanb/Sensor-Bridge-STM32-to-Cloud-via-ESP32/blob/main/configuration.png" alt="Configuration" width="500"/>

PA0 -> GPIO_Output -> DHT11 Sensor

PA1 -> ADC_IN1 -> IR Distance Sensor

PA9 -> USART1_TX --> ESP32 G16 -> RX

PA10 -> USART1_RX --> ESP32 G17 -> TX

! All the GNDs are connected.

I used this library for the DHT11 sensor -> https://github.com/quen0n/DHT11-DHT22-STM32-HAL






