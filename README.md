# 🚨 RTOS Based Smart Home Security Controller (STM32)

A real-time smart home security system built using **STM32F030R8** and **FreeRTOS**. The system detects motion and intrusion using sensors, then activates security outputs such as RGB LED, buzzer, and relay.

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
* Bread Board
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

```text
Core.zip/
Drivers.zip/
Middlewares.zip/
RTOS_Smart_Home_Security.ioc
STM32F030R8TX_FLASH.id
README.md
```

---

## ▶️ How to Run

1. Open the project in **STM32CubeIDE**
2. Build the project
3. Flash code to STM32 board
4. Connect all sensors and modules
5. Power the board
6. Observe outputs using LED, buzzer, and relay

---
## 📸 Hardware Setup & Output Explanation

### 🔧 Complete Prototype Setup

<img width="1280" height="963" alt="image" src="https://github.com/user-attachments/assets/81c52f52-5084-46bf-a2ed-c5a432ee903c" />

**Explanation:**
This image shows the full prototype implementation of the RTOS Smart Home Security Controller using the STM32 Nucleo-F030R8 board. The system is connected with PIR sensor, ultrasonic sensor, RGB LED, buzzer, relay module, and jumper wiring through the embedded trainer kit and breadboard. This setup demonstrates real hardware interfacing, sensor integration, and embedded system prototyping.

---

### 🟢 Safe State Output

<img width="1280" height="963" alt="image" src="https://github.com/user-attachments/assets/e00c4f56-27f1-4938-b804-3e2f20488364" />

**Explanation:**
The RGB LED glows green when no motion or intrusion is detected. In this mode, the system is operating normally and continuously monitoring the environment through FreeRTOS tasks. The buzzer remains OFF and the relay remains OFF.

**Condition:**

* No motion detected
* No nearby object
* System secure

---

### 🔵 Warning / Detection State

<img width="1280" height="963" alt="image" src="https://github.com/user-attachments/assets/193c6c8f-8636-49b5-9c81-c6cce16bb3a4" />

**Explanation:**
The RGB LED changes to blue when sensor activity or warning conditions are detected. This indicates that the system has identified movement or a state change and is evaluating the environment. It acts as an intermediate alert before full alarm activation.

**Condition:**

* Motion detected or object activity sensed
* Monitoring intensified
* Alarm pending based on logic

---

### 🔴 Alarm State (Add when captured)

<img width="1280" height="963" alt="WhatsApp Image 2026-04-28 at 3 14 12 PM" src="https://github.com/user-attachments/assets/4b7a2fc3-0432-4d4d-a8ac-51892292e5c2" />

**Explanation:**
In alarm mode, the RGB LED turns red, the buzzer activates, and the relay switches ON. This happens when motion and intrusion conditions are satisfied simultaneously. It represents an active security breach response.

**Condition:**

* Motion detected
* Object within threshold distance
* Security alarm triggered


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
