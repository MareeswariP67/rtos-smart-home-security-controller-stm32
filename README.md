# 🚨 RTOS Smart Home Security Controller (STM32)

A real-time smart home security system built using *STM32F030R8* and *FreeRTOS*. The system detects motion and intrusion using sensors, then activates security outputs such as RGB LED, buzzer, and relay.

---

## 🔧 Features

* ✅ PIR motion detection
* ✅ Ultrasonic intrusion sensing
* ✅ RGB LED status indication
* ✅ Buzzer alarm
* ✅ Relay trigger output
* ✅ FreeRTOS multitasking
* ✅ Real-time embedded control

---

## 🧰 Hardware Used

* STM32 Nucleo-F030R8
* PIR Sensor
* Ultrasonic Sensor
* RGB LED
* Buzzer
* Relay Module
* Jumper Wires
* USB Cable

---

## 🧠 RTOS Tasks

| Task            | Purpose                |
| --------------- | ---------------------- |
| PIR Task        | Detect motion          |
| Ultrasonic Task | Measure distance       |
| Alarm Task      | Trigger buzzer + relay |
| Status Task     | Control RGB LED        |

---

## 🚦 System States

| State   | Condition                            | Output                   |
| ------- | ------------------------------------ | ------------------------ |
| Safe    | No motion detected                   | Green LED                |
| Warning | Motion detected                      | Yellow LED               |
| Alarm   | Motion + Object distance < threshold | Red LED + Buzzer + Relay |

---

## 🔌 Pin Connections

| Component       | STM32 Pin |
| --------------- | --------- |
| PIR OUT         | PA0       |
| Ultrasonic TRIG | PA1       |
| Ultrasonic ECHO | PA2       |
| Buzzer          | PA3       |
| Relay           | PA4       |
| RGB Red         | PA5       |
| RGB Green       | PF4       |
| RGB Blue        | PF5       |

---

## 📂 Project Structure

text
Core/
Drivers/
Middlewares/
RTOS_Smart_Home_Security.ioc
README.md


---

## ▶️ How to Run

1. Open the project in *STM32CubeIDE*
2. Build the project
3. Flash code to STM32 board
4. Connect all sensors and modules
5. Power the board
6. Observe outputs using LED, buzzer, and relay

---

## 🧪 Expected Behavior

### Safe Mode

* Green LED ON
* Buzzer OFF
* Relay OFF

### Warning Mode

* Yellow LED ON
* Buzzer OFF
* Relay OFF

### Alarm Mode

* Red LED ON
* Buzzer ON
* Relay ON

---

## 💼 Skills Demonstrated

* Embedded C
* STM32 HAL Drivers
* FreeRTOS
* Task Scheduling
* GPIO Interfacing
* Sensor Integration
* Real-Time Systems
* Debugging

---

## 🚀 Future Improvements

* GSM Alert Notifications
* IoT Cloud Dashboard
* Mobile App Control
* Camera Snapshot on Intrusion
* EEPROM Event Logging

---

## 📸 Demo

Add project photos or demo videos in this repository.

---

## 👩‍💻 Author

Developed as an embedded systems project using STM32 + FreeRTOS.
