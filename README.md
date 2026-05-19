[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/AnR2QgvN)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=22925822&assignment_repo_type=AssignmentRepo)

# 🌐 IoT Elective Project 2026

### Cape Peninsula University of Technology — IT Diploma

**Module:** Internet of Things (IoT) Elective | **Year:** 2026

---

# 📋 Table of Contents

1. Project Overview
2. Group Members
3. Project Idea & Problem Statement
4. System Architecture & Design
5. Hardware Components
6. Software & Technologies
7. Circuit Diagram / Wiring
8. Build Process (with photos)
9. Code Documentation
10. Testing & Results
11. Challenges & Solutions
12. Project Demonstration
13. References
14. Assessment Rubric

---

# 📌 Project Overview

**Project Title:** `Smart Attendance System`  
**Group Name / Number:** `Fantastic Four`  
**Presentation Date:** `20 May 2026`

---

# 👥 Group Members

| Student Name | Student Number | Role / Responsibility |
|---|---|---|
| Redah Gamieldien | 222641681 | Testing Lead |
| Lyle Solomons | 230123872 | Software Lead |
| Qaasim Isaacs | 222544422 | Hardware Lead |
| Ethan Williams | 221454780 | Documentation Lead |

---

# 💡 Project Idea & Problem Statement

## Problem Statement

Currently, student identification cards are mainly used only to access campus facilities. However, classroom attendance is still recorded manually using attendance sheets.

This creates several problems:

- Attendance sheets can be lost or damaged
- Students may sign attendance for absent friends
- Manual attendance recording is time consuming
- Attendance tracking becomes unreliable and prone to human error

Because of these issues, there is a need for a smarter and more efficient attendance system.

---

## Proposed Solution

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

## Objectives

1. Track student attendance automatically and accurately  
2. Help lecturers manage attendance records more efficiently  
3. Reduce human error and fraudulent attendance marking  
4. Demonstrate the use of IoT technology in a real-world educational environment  

---

# 🏗️ System Architecture & Design

![System Architecture](image/System_Architecture.png)

## Design Decisions

- ESP32 was selected as the main controller because it supports both RFID communication and built-in Wi-Fi connectivity.
- MFRC522 RFID module was chosen for fast and contactless student identification.
- SPI communication was implemented between the ESP32 and RFID module for reliable data transfer.
- LEDs and a buzzer were added to provide instant visual and audio feedback.
- GitHub was used for version control and documentation.
- The system supports real-time attendance recording.
- Breadboard prototyping was used for testing.
- The design is scalable for future classroom expansion.

---

# 🔧 Hardware Components

| Component | Description | Quantity | Purpose |
|---|---|---|---|
| ESP32 Development Board | Microcontroller with Wi-Fi | 1 | Main controller |
| MFRC522 RFID Module | RFID reader | 1 | Reads student cards |
| RFID Cards | Student tags | Multiple | Attendance identification |
| Green LED | Indicator LED | 1 | Success signal |
| Red LED | Indicator LED | 1 | Failure signal |
| Active Buzzer | Sound output | 1 | Audio feedback |
| 220Ω Resistors | Protection | 2 | LED protection |
| Jumper Wires | Connections | Multiple | Wiring |
| Breadboard | Prototype board | 1 | Circuit testing |
| Enclosure | Housing | 1 | Final protection |

---

# 💻 Software & Technologies

| Tool | Purpose |
|---|---|
| Arduino IDE | Programming ESP32 |
| GitHub | Version control |
| Wokwi | Simulation |
| C++ | Firmware language |
| ESP32 Wi-Fi Library | Connectivity |
| MFRC522 Library | RFID communication |

---

# 🔌 Circuit Diagram / Wiring

![Circuit Diagram](image/Circuit_Diagram.jpeg)

| Component Pin | ESP32 Pin |
|---|---|
| SDA | GPIO 5 |
| SCK | GPIO 18 |
| MOSI | GPIO 23 |
| MISO | GPIO 19 |
| RST | GPIO 22 |
| VCC | 3.3V |
| GND | GND |
| Green LED | GPIO 13 |
| Red LED | GPIO 12 |
| Buzzer | GPIO 14 |

---

# 🏭 Build Process

## Step 1: ESP32 Setup
![Step 1](image/1.jpeg)

## Step 2: RFID Module
![Step 2](image/2.jpeg)

## Step 3: SPI Connection
![Step 3](image/3.jpeg)

## Step 4: Green LED
![Step 4](image/4.jpeg)

## Step 5: Red LED
![Step 5](image/5.jpeg)

## Step 6: Buzzer
![Step 6](image/6.jpeg)

## Step 7: Testing Connections
![Step 7](image/7.jpeg)

## Step 8: Upload Code
![Step 8](image/8.jpeg)

## Step 9: Final Build
![Step 9](image/9.jpeg)

## Step 10: Final UI Dashboard
![Step 10](image/10.jpeg)

## Step 11: Housing Unit Components
![Step 11](image/11.jpeg)

## Step 12: Complete Housing Unit Assembly
![Step 12](image/12.jpeg)



# 🖥️ Code Documentation

## Main Firmware (`main.ino`)

## Key Functions

| Function Name | Description |
|---|---|

---

# 🧪 Testing & Results

| Test # | Description | Expected Result | Actual Result | Pass/Fail |
|---|---|---|---|---|
| 1 | ESP32 startup | Works | Works | ✅ |
| 2 | RFID detection | Detects card | Works after delay | ✅ |
| 3 | UID transfer | Accurate | Correct after retry | ✅ |
| 4 | Green LED | On success | Works | ✅ |
| 5 | Red LED | On failure | Works | ✅ |
| 6 | Buzzer | Sound output | Fixed after wiring | ✅ |
| 7 | Resistors | Safe LED use | Stable | ✅ |
| 8 | SPI communication | Stable | One timeout recovered | ✅ |
| 9 | Full system | Works together | Works after fixes | ✅ |

---

# ⚠️ Challenges & Solutions

| Challenge | Solution |
|---|---|
| ESP32 crashing | Fixed code logic |
| RFID not reading | Fixed wiring |
| Inconsistent scans | Added delays |
| LEDs not working | Fixed GPIO wiring |
| Weak buzzer | Fixed polarity |
| Upload issues | Fixed COM port |

---

# 🎥 Project Demonstration

- Video: [Insert link]
- Slides: [Insert link]
- GitHub: [Insert link]

---

# 📚 References

1. ESP32 Documentation – https://docs.espressif.com/projects/esp-idf/en/latest/esp32/
2. MFRC522 Library – https://github.com/miguelbalboa/rfid
3. Arduino IDE – https://www.arduino.cc/en/software
4. Wokwi – https://wokwi.com/

---

# 📊 Assessment Rubric

*(Do not modify this section)*

### T1 — 50 Marks
| Criteria | Marks |
|---|---|

### T2 — 50 Marks
| Criteria | Marks |
|---|---|

---

# 🏆 Final Mark Summary

| Term | Marks |
|---|---|
| T1 | /50 |
| T2 | /50 |
| Total | /100 |

---

**Assessed by:** Lecturer Name  
**Deadline:** April 2026  
**Institution:** Cape Peninsula University of Technology (CPUT)
