# System Requirements

## 1. Project objective

The Medical Monitoring System (ESP32) is an embedded IoT prototype that monitors temperature and simulated heart rate.

The system displays measurements locally, identifies abnormal values, activates alarms, and transmits data to a remote dashboard through Wi-Fi.

> This project is an educational prototype and is not a certified medical device.

## 2. Functional requirements

### FR-01 — Temperature measurement

The system shall read the temperature from a DHT22 sensor.

### FR-02 — Heart-rate simulation

The system shall use a potentiometer to simulate a heart-rate sensor during the Wokwi simulation.

### FR-03 — Local display

The system shall display the temperature and heart rate on an SSD1306 OLED screen.

### FR-04 — Normal status

The system shall activate the green LED when all measurements are within their normal ranges.

### FR-05 — Alarm status

The system shall activate the red LED and buzzer when at least one measurement is outside its normal range.

### FR-06 — Wi-Fi communication

The ESP32 shall connect to a Wi-Fi network.

### FR-07 — Remote monitoring

The system shall transmit measurements to an IoT dashboard.

### FR-08 — Measurement history

The dashboard shall display the history of the transmitted measurements.

### FR-09 — Event logging

The system shall record abnormal measurements and connection errors.

## 3. Operating conditions

For this educational prototype, the following thresholds will be used:

| Measurement | Normal range | Abnormal condition |
|---|---:|---:|
| Temperature | 36.0–37.5 °C | Below 36.0 °C or above 37.5 °C |
| Heart rate | 60–100 BPM | Below 60 BPM or above 100 BPM |

The thresholds are configurable and are used only to demonstrate the alarm logic.

## 4. Technical requirements

- ESP32 development board
- Arduino framework with C++
- Wokwi simulation platform
- DHT22 temperature sensor
- Potentiometer for simulated heart rate
- SSD1306 OLED display
- Green LED
- Red LED
- Buzzer
- Wi-Fi connection
- IoT dashboard

## 5. Non-functional requirements

- The source code shall be organized into understandable modules.
- Important functions and decisions shall be documented.
- The system shall update the measurements without blocking its main operation.
- Sensor and connection errors shall be handled safely.
- No personal or confidential health data shall be stored.
- The project shall include documented test cases.

## 6. Acceptance criteria

- [ ] Temperature is read and displayed.
- [ ] Simulated heart rate is calculated and displayed.
- [ ] The green LED indicates normal measurements.
- [ ] The red LED and buzzer indicate abnormal measurements.
- [ ] The ESP32 connects to Wi-Fi.
- [ ] Measurements appear on the dashboard.
- [ ] Normal, abnormal and error conditions are tested.
- [ ] The project documentation explains the system and its limitations.