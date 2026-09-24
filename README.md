## EXP — INTERFACING A 16×2 LCD WITH ARDUINO USING AN I2C MODULE FOR SENSOR DATA DISPLAY

## Aim

To interface a **16×2 LCD display with Arduino using an I2C module** and display sensor data on the LCD.

## Objectives

- To understand the operation of a 16×2 LCD.
- To interface the LCD with Arduino using an I2C module.
- To reduce the number of GPIO pins required for LCD communication.
- To read sensor data using Arduino.
- To display the sensor readings on the LCD.

## Hardware / Software Tools Required

### Hardware

- Arduino UNO
- 16×2 LCD Display
- I2C LCD Module (PCF8574-based)
- DHT11 Temperature and Humidity Sensor
- Breadboard
- Jumper wires
- USB cable

### Software

- Arduino IDE
- Arduino C/C++ programming language
- LiquidCrystal_I2C library
- DHT sensor library

## Components

 16×2 LCD
 I2C Module
 Circuit Connections
 I2C Communication
 Working Principle

1. The DHT11 sensor measures temperature and humidity.
2. Arduino reads the sensor values through the digital data pin.
3. The Arduino processes the received sensor data.
4. The processed values are sent to the LCD through the I2C interface.
5. The LCD displays the temperature on one line.
6. The humidity is displayed on the second line.
7. The readings are periodically updated.

## Arduino Program

    #include <Wire.h>
    #include <LiquidCrystal_I2C.h>

    LiquidCrystal_I2C lcd(0x27, 16, 2); // I2C address 0x27, 16x2 LCD

    void setup() {
      lcd.init();           // Initialize the LCD
      lcd.backlight();      // Turn on backlight
      lcd.clear();          // Clear any previous text
      lcd.setCursor(4, 0);  // Set cursor position (column 4, row 0)
      lcd.print("SUJHAN");  // Display text
    }

    void loop() {
      // Nothing here — static display
    }



## Observation

<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/31de352b-34f3-4d2b-8efa-dd3fd7e972c0" />

<img width="1280" height="964" alt="image" src="https://github.com/user-attachments/assets/c097f9f1-d5e2-476e-828b-c2a3003ea4cc" />




## Result

Thus, the **16×2 LCD was successfully interfaced with Arduino UNO using an I2C module**, and the temperature and humidity values obtained from the DHT11 sensor were successfully displayed on the LCD. The experiment demonstrates the use of **I2C communication for efficient sensor-data display** in embedded and IoT applications.
