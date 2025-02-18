# 🌿 Air Quality Monitoring System with LCD 🌿

This project uses an air quality sensor, an Arduino (or compatible microcontroller), and an LCD to monitor and display the air quality. The system reads air quality values from an analog sensor, categorizes the air quality, and displays the results on an LCD screen. It also outputs the air quality to the serial monitor for debugging.

## Components Required:
- Arduino (or compatible microcontroller)
- Air quality sensor (analog output)
- 16x2 LCD (LiquidCrystal display)
- Jumper wires
- Breadboard
- Digital output device (optional, such as a fan)

## Libraries Used:
- `LiquidCrystal` library: Used for controlling the LCD display.

## Pin Configuration:
- **LCD Pins:**
  - Pin 12: RS
  - Pin 11: Enable
  - Pin 5: D4
  - Pin 4: D5
  - Pin 3: D6
  - Pin 2: D7
- **Analog Pin:**
  - Pin A0: Air quality sensor (analog input)
- **Digital Pin:**
  - Pin 8: Digital output (for controlling a device, e.g., a fan)

## Working:
- The air quality sensor provides an analog value that is read by the microcontroller through pin `A0`.
- The system categorizes the air quality based on the sensor's value:
  - **Fresh Air:** If the sensor value is ≤ 500
  - **Poor Air:** If the sensor value is between 500 and 650
  - **Very Poor Air:** If the sensor value is > 650
- The air quality level is displayed on a 16x2 LCD.
- If the air quality is "Very Poor" (sensor value > 650), a digital pin is activated, which can be used to control a connected device like a fan.
- The air quality is also printed to the serial monitor for debugging purposes.

## Code Explanation:

1. **LCD Initialization:** The `LiquidCrystal` library is initialized with the required pins for controlling the LCD.
2. **Sensor Reading:** The analog value from the sensor is read using `analogRead()`.
3. **Air Quality Categorization:** Based on the sensor value, the air quality is categorized into three levels: "Fresh Air", "Poor Air", and "Very Poor Air".
4. **LCD Output:** The categorized air quality is displayed on the LCD.
5. **Digital Output:** If the air quality is "Very Poor", pin 8 is activated to control an external device.

## How to Use:

1. Connect the air quality sensor to pin `A0` of the Arduino.
2. Connect the LCD to the specified pins (12, 11, 5, 4, 3, 2).
3. If desired, connect a fan or other device to pin 8 to activate when the air quality is very poor.
4. Upload the code to the Arduino and open the serial monitor to see the air quality in PPM.
5. The LCD will display the air quality status, and the digital output pin will be activated if necessary.

## Troubleshooting:
- **LCD not displaying correctly:** Ensure all the LCD connections are made properly and the `LiquidCrystal` library is installed.
- **Inaccurate air quality readings:** Make sure the air quality sensor is calibrated and functioning properly.
- **Serial monitor not showing data:** Ensure the baud rate is set to 9600 in the serial monitor and that the Arduino is connected correctly.

## License:
This project is open-source and available under the MIT License.

