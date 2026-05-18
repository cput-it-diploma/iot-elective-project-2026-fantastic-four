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

**Project Title:** `Smart Attendence System`  
**Group Name / Number:** `Fantastic Four`  
**Presentation Date:** 20 May 2026

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
Currently, student identification cards serve only a single purpose and is grant access to campus facilities. Classroom attendance, however, is still recorded manually by writing names on a sheet of paper.
This raises many problems like:
-	The attendance sheet could get lost or damaged
-	Some students will sign for their absent friends
-	It is time consuming to record and verify student attendance
This results in tracking student attendance being unreliable, inefficient and it is prone to human error. This system needs to be updated with a more accurate system.


### Proposed Solution
We propose the development of a Smart Attendance System that integrates RFID technology with cloud-based monitoring.
This system will be installed in every classroom and will function as follows:
-	Students must tap their RFID enabled student cards on the reader
-	The system will automatically record their attendance
-	Visual (LED) and buzzer indicators will confirm successful or failed scans.
-	Attendance data will be uploaded in real-time to a cloud dashboard using ThingSpeak for temporary storage and monitoring
-	Each record will include student ID and timestamp using a Real-Time Clock (RTC) module for accuracy.


### Objectives
1. Track Student attendance
2.	Manage attendance records for lecturers accurately


---

## 🏗️ System Architecture & Design

![System Architecture Diagram](images/architecture_diagram.png)

### Design Decisions
> _Explain the key design decisions your group made._

---

## 🔧 Hardware Components

| Component | Description | Quantity | Purpose |
|---|---|---|---|
| ESP32 Development Board | Microcontroller with built-in Wi-Fi and Bluetooth | 1 | Main controller that processes RFID data, controls peripherals, and sends attendance data to ThingSpeak |
| MFRC522 RFID Module | 13.56 MHz RFID reader using SPI communication | 1 | Reads student RFID cards and sends unique ID to ESP32 |
| RFID Student Cards / Tags | Passive 13.56 MHz RFID cards | Multiple | Used by students to scan and register attendance |
| 5mm Bi-colour LED (Green/Red) | Dual-colour LED | 1 of each | Provides visual feedback for valid (green) and invalid (red) scans |
| DB-111G Buzzer | Active buzzer | 1 | Provides audio feedback for scan validation |
| Resistors (220Ω or 330Ω) | Current-limiting resistors | 1 | Protects LED from excessive current |
| Jumper Wires | Male-Male / Male-Female connection wires | Multiple | Electrical connections between components |
| Breadboard | Prototyping board | 1 | Temporary circuit assembly during development |
| Enclosure Casing | Protective housing | 1 | Secures and protects system for classroom installation |

---

## 💻 Software & Technologies

| Tool / Platform | Purpose |
|---|---|
| [e.g. Arduino IDE] | [Firmware development] |
| [e.g. MQTT / Node-RED] | [Data communication / dashboard] |
| [e.g. GitHub] | [Version control & documentation] |
| [e.g. Fritzing] | [Circuit design] |

---

## 🔌 Circuit Diagram / Wiring

![Circuit Diagram](images/circuit_diagram.png)

| Component Pin | Microcontroller Pin | Notes |
|---|---|---|
| [e.g. DHT11 DATA] | [e.g. D2] | [Pull-up resistor required] |
| [e.g. LED +] | [e.g. D13] | [220Ω resistor in series] |

---

## 🏭 Build Process (with photos)

### Step 1: [Step Title]
> _Description of what was done._

![Step 1 Photo](images/build_step1.jpg)

### Step 2: [Step Title]
> _Description of what was done._

![Step 2 Photo](images/build_step2.jpg)

---

## 🖥️ Code Documentation

### Main Firmware (e.g., `main.ino`)

```cpp
void setup() {
  Serial.begin(9600);
  // Initialize sensors and pins here
}

void loop() {
  // Main logic here
}
```

### Key Functions

| Function Name | Description |
|---|---|
| `setup()` | Initializes hardware peripherals and serial communication |
| `loop()` | Main execution loop |
| `[yourFunction()]` | [Describe it] |

---

## 🧪 Testing & Results

| Test # | Description | Expected Result | Actual Result | Pass/Fail |
|---|---|---|---|---|
| 1 | [e.g. Sensor reads temperature] | [e.g. ±2°C accuracy] | [e.g. ±1.5°C] | ✅ Pass |
| 2 | [e.g. Wi-Fi transmission] | [e.g. Every 10s] | | |

---

## ⚠️ Challenges & Solutions

| Challenge Encountered | Solution Applied |
|---|---|
| [e.g. Wi-Fi connection drops] | [e.g. Added reconnect logic] |
| [e.g. Noisy sensor readings] | [e.g. Applied moving average filter] |

---

## 🎥 Project Demonstration

- 📹 **Demo Video:** [Insert link here]
- 📊 **Presentation Slides:** [Insert link here]
- 🔗 **Live Dashboard (if applicable):** [Insert link here]

---

## 📚 References

1. [Reference Title](https://link-to-reference.com) — _Brief description_
2. [Reference Title](https://link-to-reference.com) — _Brief description_

---

## 📊 Assessment Rubric

> ⚠️ **Students: Do NOT modify this section.**

### 📝 T1 — 50 Marks

| Criteria | Excellent (5) | Good (4) | Satisfactory (3) | Needs Improvement (2) | Incomplete (0-1) | Marks |
|---|---|---|---|---|---|---|
| Project Proposal & Problem Statement | Clear, detailed, well-researched | Clear with minor gaps | Stated but lacks depth | Vague | Not submitted | /5 |
| System Design & Architecture | Detailed diagram + design decisions | Good diagram with some docs | Basic diagram | Incomplete | Not submitted | /5 |
| Hardware Component Selection | All justified with images | Most documented | Listed not justified | Incomplete | Not attempted | /5 |
| Circuit Diagram / Wiring | Complete + pin mapping | Mostly complete | Partial | Incomplete | Not submitted | /5 |
| GitHub Repository Setup | Well-structured, clear commits | Good with minor issues | Basic structure | Minimal | Repo not set up | /5 |
| Markdown Documentation Quality | Excellent: headings, tables, images, code | Good with minor issues | Basic Markdown | Minimal | None | /5 |
| GitHub Commit History (T1) | Regular commits, all members | Regular, most members | Some commits | Few | None | /5 |
| Initial Code / Prototype | Working + well-commented | Working + some comments | Partial prototype | Started, not working | None | /5 |
| Group Collaboration Evidence | Issues, PRs, commits from all | Good evidence | Some evidence | Minimal | None | /5 |
| Build Progress Photos | Step-by-step + descriptions | Good photos | Photos, few descriptions | Few photos | None | /5 |
| | | | | | **T1 Total** | **/50** |

---

### 📝 T2 — 50 Marks *(Final Presentation: End of April 2026)*

| Criteria | Excellent (5) | Good (4) | Satisfactory (3) | Needs Improvement (2) | Incomplete (0-1) | Marks |
|---|---|---|---|---|---|---|
| Final Working Project | Fully functional | Mostly functional | Partially functional | Limited functionality | Not functional | /5 |
| Live Demonstration | Confident, all features | Good, minor issues | Core features shown | Partial/unclear | No demonstration | /5 |
| Testing & Results Documentation | All tests + analysis | Most documented | Some documented | Minimal | None | /5 |
| Code Quality & Comments | Clean, structured, fully commented | Good, most commented | Works, lacks comments | Messy/partial | None | /5 |
| Markdown Documentation Quality (T2) | Complete professional README | Good with minor gaps | Most sections filled | Incomplete | Minimal/none | /5 |
| GitHub Commit History (T2) | Consistent, all members | Good, most members | Some commits | Few | None | /5 |
| Challenges & Solutions | All documented with solutions | Most documented | Some documented | Vague | Not documented | /5 |
| System Architecture (Final) | Updated, matches build | Mostly matches | Partially updated | Outdated | Not present | /5 |
| Presentation Quality | Professional, all members | Good, all contribute | Acceptable | Weak/incomplete | None | /5 |
| References & Attribution | All properly listed | Most listed | Some listed | Minimal | None | /5 |
| | | | | | **T2 Total** | **/50** |

---

### 🏆 Final Mark Summary

| Term | Marks Available | Marks Achieved |
|---|---|---|
| T1 | 50 | /50 |
| T2 | 50 | /50 |
| **Total** | **100** | **/100** |

---

> 📌 **Assessed by:** `[Lecturer Name]`  
> 📅 **Final Submission Deadline:** End of April 2026  
> 🏫 **Institution:** Cape Peninsula University of Technology (CPUT)

---

*Documented using Markdown on GitHub — CPUT IT Diploma IoT Elective 2026* 🚀
