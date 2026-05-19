[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/AnR2QgvN)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=22925822&assignment_repo_type=AssignmentRepo)

# 🌐 IoT Elective Project 2026
### Cape Peninsula University of Technology — IT Diploma
**Module:** Internet of Things (IoT) Elective | **Year:** 2026

---

## 📋 Table of Contents

1. [Project Overview](#project-overview)
2. [Group Members](#group-members)
3. [Project Idea & Problem Statement](#project-idea--problem-statement)
4. [System Architecture & Design](#system-architecture--design)
5. [Hardware Components](#hardware-components)
6. [Software & Technologies](#software--technologies)
7. [Circuit Diagram / Wiring](#circuit-diagram--wiring)
8. [Build Process (with photos)](#build-process-with-photos)
9. [Code Documentation](#code-documentation)
10. [Testing & Results](#testing--results)
11. [Challenges & Solutions](#challenges--solutions)
12. [Project Demonstration](#project-demonstration)
13. [References](#references)
14. [Assessment Rubric](#assessment-rubric)

---

## 📌 Project Overview

**Project Title:** `Smart Attendance System`  
**Group Name / Number:** `Fantastic Four`  
**Presentation Date:** `20 May 2026`

---

## 👥 Group Members

| Student Name | Student Number | Role / Responsibility |
|---|---|---|
| Redah Gamieldien | 222641681 | Documentation Lead |
| Lyle Solomons | 230123872 | Software Lead |
| Qaasim Isaacs | 222544422 | Hardware Lead |
| Ethan Williams | 221454780 | Testing Lead |

---

## 💡 Project Idea & Problem Statement

### Problem Statement

Currently, student identification cards are mainly used only to access campus facilities. However, classroom attendance is still recorded manually using attendance sheets.

This creates several problems:

- Attendance sheets can be lost or damaged
- Students may sign attendance for absent friends
- Manual attendance recording is time consuming
- Attendance tracking becomes unreliable and prone to human error

Because of these issues, there is a need for a smarter and more efficient attendance system.

---

### Proposed Solution

We developed a **Smart Attendance System** that integrates RFID technology with cloud-based monitoring.

The system functions as follows:

- Students scan their RFID-enabled student cards on the RFID reader
- The ESP32 processes the card information
- The system automatically records attendance
- LED indicators and a buzzer provide visual and audio feedback for successful or failed scans
- Attendance data is uploaded in real-time using Wi-Fi communication
- GitHub is used for project hosting, documentation, and monitoring progress

This allows attendance to be monitored digitally, accurately, and efficiently.

---

### Objectives

1. Track student attendance automatically and accurately
2. Help lecturers manage attendance records more efficiently
3. Reduce human error and fraudulent attendance marking
4. Demonstrate the use of IoT technology in a real-world educational environment

## 🏗️ System Architecture & Design

![System Architecture Diagram](image/System_Architecture.png)

### Design Decisions

- ESP32 was selected as the main controller because it supports both RFID communication and built-in Wi-Fi connectivity.
- MFRC522 RFID module was chosen for fast and contactless student identification.
- SPI communication was implemented between the ESP32 and RFID module for reliable data transfer.
- LEDs and a buzzer were added to provide instant visual and audio feedback to users.
- GitHub was used for version control, documentation, and project management.
- The system was designed to support real-time attendance recording.
- Breadboard prototyping was used to simplify hardware testing and troubleshooting.
- The project was designed to be scalable for future classroom expansion.

---

## 🔌 Circuit Diagram / Wiring

![Circuit Diagram](image/Circuit_Diagram.jpeg)

| Component Pin | Microcontroller Pin | Notes |
|---|---|---|
| MFRC522 SDA (SS) | GPIO 5 | SPI Slave Select pin |
| MFRC522 SCK | GPIO 18 | SPI Clock |
| MFRC522 MOSI | GPIO 23 | SPI Master Out Slave In |
| MFRC522 MISO | GPIO 19 | SPI Master In Slave Out |
| MFRC522 RST | GPIO 22 | RFID Reset pin |
| MFRC522 VCC | 3.3V | RFID module powered from ESP32 |
| MFRC522 GND | GND | Common ground |
| Green LED (+) | GPIO 13 | Use 220Ω resistor in series |
| Green LED (-) | GND | Ground connection |
| Red LED (+) | GPIO 12 | Use 220Ω resistor in series |
| Red LED (-) | GND | Ground connection |
| Buzzer (+) | GPIO 14 | Active buzzer for scan feedback |
| Buzzer (-) | GND | Common ground |

---

## 🏭 Build Process (with photos)

### Step 1: Install ESP32 to Breadboard

> Inserted the ESP32 development board into the breadboard for the main hardware setup.

![Step 1 Photo](image/1.jpeg)

---

### Step 2: Install MFRC522 RFID Scanner

> Mounted the MFRC522 RFID module onto the breadboard.

![Step 2 Photo](image/2.jpeg)

---

### Step 3: Connect ESP32 to RFID Scanner

> Connected SPI communication pins between ESP32 and MFRC522 module.

![Step 3 Photo](image/3.jpeg)

---

### Step 4: Install Green LED

> Connected the green LED with a 220Ω resistor for successful scan indication.

![Step 4 Photo](image/4.jpeg)

---

### Step 5: Install Red LED

> Connected the red LED with a 220Ω resistor for invalid scan indication.

![Step 5 Photo](image/5.jpeg)

---

### Step 6: Mount the Buzzer

> Installed the active buzzer for audio feedback during scans.

![Step 6 Photo](image/6.jpeg)

---

### Step 7: Test Hardware Connections

> Verified all hardware connections and checked for communication errors.

![Step 7 Photo](image/7.jpeg)

---

### Step 8: Upload Firmware to ESP32

> Uploaded the attendance system firmware using Arduino IDE.

![Step 8 Photo](image/8.jpeg)

---

### Step 9: Final Hardware Setup

> Completed final hardware assembly and enclosure installation.

![Step 9 Photo](image/9.jpeg)

---

### Step 10: Final UI dashboard

---
### Step 11: Components for the housing case
![Step 11 Photo](images/11.jpeg)
---
### Step 12: Completed housing case
![Step 12 Photo](images/12.jpeg)
---

## 🖥️ Code Documentation

### Main Firmware (e.g., `main.ino`)


### Key Functions


---

## 🧪 Testing & Results

| Test # | Description | Expected Result | Actual Result | Pass/Fail |
|---|---|---|---|---|
| 1 | ESP32 powers on and connects to system | ESP32 initializes successfully | ESP32 booted successfully after first restart attempt | ✅ Pass |
| 2 | MFRC522 RFID scanner detects RFID card | RFID card detected within 2 seconds | Initial scan delay of 3 seconds, then successful detection | ✅ Pass |
| 3 | RFID data transmission to ESP32 | UID transmitted accurately | First read returned incomplete UID, second read successful | ✅ Pass |
| 4 | Green LED indication for valid card | Green LED lights up on authorized scan | LED flickered briefly before remaining stable | ✅ Pass |
| 5 | Red LED indication for invalid card | Red LED lights up on unauthorized scan | Worked correctly after resistor connection adjustment | ✅ Pass |
| 6 | Active buzzer audio feedback | Buzzer sounds during scan | Sound volume was initially low, corrected after rewiring | ✅ Pass |
| 7 | 220Ω resistor protection for Green LED | LED brightness controlled safely | No overheating detected during testing | ✅ Pass |
| 8 | 220Ω resistor protection for Red LED | Stable LED operation | Minor flicker observed initially, later stabilized | ✅ Pass |
| 9 | SPI communication between ESP32 and MFRC522 | Continuous communication without interruption | Temporary communication timeout occurred once, auto-recovered | ✅ Pass |
| 10 | Full attendance system operation | All components operate together correctly | System completed scans and feedback successfully after minor troubleshooting | ✅ Pass |

---

## ⚠️ Challenges & Solutions

| Challenge Encountered | Solution Applied |
|---|---|
| ESP32 crashing during startup due to code error | Debugged and corrected faulty code logic in Arduino IDE |
| MFRC522 RFID scanner not detecting cards | Rechecked SPI wiring connections and corrected misplaced pins |
| RFID reader giving inconsistent scans | Added delays and improved scan handling logic |
| Red LED not turning on properly | Fixed loose jumper wire connection and verified GPIO pin assignment |
| Green LED flickering during scans | Added proper 220Ω resistor and stabilized power connection |
| Active buzzer producing weak sound | Corrected buzzer polarity and updated output timing |
| ESP32 failing to upload code | Selected correct COM port and ESP32 board configuration |

---

## 🎥 Project Demonstration

- 📹 **Demo Video:** [Insert link here]
- 📊 **Presentation Slides:** [Insert link here]
- 🔗 **GitHub Repository:** [Insert link here]

---

## 📚 References

1. [ESP32 Documentation](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/) — Official ESP32 documentation  
2. [MFRC522 RFID Library](https://github.com/miguelbalboa/rfid) — RFID library for Arduino and ESP32  
3. [Arduino IDE](https://www.arduino.cc/en/software) — Arduino development environment  
4. [Wokwi](https://wokwi.com/) — Online IoT simulation and circuit testing platform
---

## 📊 Assessment Rubric

> ⚠️ **Students: Do NOT modify this section.**

[KEEP THE REST OF YOUR RUBRIC SECTION EXACTLY AS IT IS]

---

> 📌 **Assessed by:** `[Lecturer Name]`  
> 📅 **Final Submission Deadline:** End of April 2026  
> 🏫 **Institution:** Cape Peninsula University of Technology (CPUT)

---

*Documented using Markdown on GitHub — CPUT IT Diploma IoT Elective 2026* 🚀
