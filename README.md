# Microcontroller-Driven Offline Weighing System  
  
**Developed by Anis Mulla**  

---

## Overview  
This project is an offline weighing system designed to automate the recording of children’s weight data using a microcontroller. It validates a child’s Unique Identification Number (UID) against a pre-stored database, measures their weight, and logs the data with timestamps into date-specific files on an SD card. Ideal for schools, healthcare providers, and NGOs for efficient health monitoring.

---

## Key Features  
- **UID Validation**: Cross-checks entered UID with a pre-stored `student_information.csv` file.  
- **Date-Specific Logging**: Automatically creates daily CSV files (e.g., `2024-05-20.csv`) for organized data storage.  
- **Offline Operation**: No internet dependency—uses SD card for data storage.  
- **Real-Time Clock (RTC)**: Timestamps entries for accurate tracking.  
- **User-Friendly Interface**: 16x2 LCD for prompts and feedback.  

---

## Hardware Requirements  
| Component               | Specification                     |  
|-------------------------|-----------------------------------|  
| Microcontroller         | Arduino Uno/Mega                 |  
| Weight Sensor           | HX711 + Load Cell (e.g., 10kg)   |  
| Input                   | 4x4 Matrix Keypad                |  
| Storage                 | SD Card Module                   |  
| Display                 | I2C 16x2 LCD                     |  
| Real-Time Clock (RTC)   | DS3231 Module                    |  
| Power Supply            | 9V Battery/DC Adapter            |  

---

## Software Requirements  
1. **Arduino IDE** (v2.0+).  
2. **Libraries**:  
   - `HX711` (by Bogdan Necula)  
   - `Keypad` (by Mark Stanley)  
   - `SD` (Built-in Arduino Library)  
   - `RTClib` (by Adafruit)  
   - `LiquidCrystal_I2C` (by Frank de Brabander)  
3. **SD Card Files**:  
   - `student_information.csv`: Pre-stored UID and student names.  
   - Date-specific `.csv` files (auto-generated).  

---

## Circuit Diagram  

### Pin Connections  
| Component          | Arduino Pin |  
|--------------------|-------------|  
| HX711 DOUT         | A0          |  
| HX711 SCK          | A1          |  
| Keypad Rows        | 2, 3, 4, 5  |  
| Keypad Columns     | 6, 7, 8, 9  |  
| SD Card CS         | 10          |  
| I2C SDA            | A4          |  
| I2C SCL            | A5          |  
| RTC SDA            | A4          |  
| RTC SCL            | A5          |  

---

## Installation & Setup  
1. **Clone the Repository**:  
   ```bash  
   git clone https://github.com/yourusername/offline-weighing-system.git  
   cd offline-weighing-system  
