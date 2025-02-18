# 🌿 Air Quality Monitoring System with LCD 🌿

This project monitors air pollution levels using an **MQ2 gas sensor, LCD, LED, and Buzzer**. If pollution crosses a certain threshold, an LED and buzzer alert the user while the LCD displays the gas level.

## 🔹 Components Used:
- **Arduino Uno**
- **MQ2 Gas Sensor**
- **16x2 LCD Display (I2C)**
- **LED (Indicates high pollution)**
- **Buzzer (Alarm for bad air quality)**
- **Resistors and Jumper Wires**

## 🔌 Wiring:
### **MQ2 Gas Sensor**
| Pin | Arduino |
|-----|---------|
| **A1** | **A0** |
| **H1** | **5V** |
| **H2** | **GND** |
| **B1** | **Pin 7 (Optional)** |

### **LCD (16x2 I2C)**
| LCD Pin | Arduino |
|---------|---------|
| **VCC** | **5V** |
| **GND** | **GND** |
| **SDA** | **A4** |
| **SCL** | **A5** |

## 📝 Code:
- Reads **gas concentration** from MQ2 sensor.
- Displays gas level **on LCD & Serial Monitor**.
- Alerts user with **LED & Buzzer** if pollution is too high.

## 🚀 Setup Instructions:
1. Connect the components as per the wiring diagram.
2. Upload the **Arduino code**.
3. Open Serial Monitor to view **gas concentration**.
4. If values exceed the threshold, the **LED & buzzer will activate**, and the **LCD will show a warning**.

## 📜 License:
This project is **open-source** and **free to use**.
