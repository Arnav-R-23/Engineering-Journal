# 💪 Engineering Journal – WRO Future Engineers 2025

**Team Name**: MakerWorks Lab  
**Institution**: [Your School/College Name]  
**Country**: India

## 📃 Table of Contents

- [👥 The Team](#the-team)
- [🌟 Challenge Overview](#challenge-overview)
- [🧐 Design & Build](#design--build)
- [🚗 Mobility & Steering](#mobility--steering)
- [🛠️ Power & Sensors](#power--sensors)
- [🔧 Assembly & Testing](#assembly--testing)
- [🔎 Obstacle Handling](#obstacle-handling)
- [📉 Cost Breakdown](#cost-breakdown)

---

## 👥 The Team

| Name          | Role              | Responsibilities                               |
| ------------- | ----------------- | ---------------------------------------------- |
| Vinay Ummadi  | Coach             |                                                |
| Kiara Bhandari| Participant       |                                                |
| Shubh Gupta   | Participant       |                                                |
| Arnav Ramteke | Participant       |         |

_Add Team Photo Here:_  
`![Team Photo](media/team_photo.jpg)`

---

## 🌟 Challenge Overview

The WRO 2025 Future Engineers challenge required teams to develop an autonomous electric vehicle that can navigate a randomized racetrack using computer vision and sensors, execute three laps, avoid obstacles, interpret traffic markers (red/green), and complete parallel parking.

---

## 🧐 Design & Build

### Chassis & Mounting

- Fully 3D-printed lightweight frame.
- Integrated mounts for camera, motor, and PCB.
- Modular component slots for easy maintenance.

_Add Robot Chassis Image:_  
`![Chassis Top View](media/chassis_top.jpg)`

### Key Features

- **Balanced Weight Distribution**: Centralized LiPo battery.
- **Wiring Management**: Routed under PCB with hot glue for strain relief.
- **Compact Design**: Ensured eligibility under size constraints.

---

## 🚗 Mobility & Steering

### Drive System

- **Motor**: Pololu 30:1 Micro Metal Gearmotor (12V).  
  `![Pololu Motor](media/motor.jpg)`
- **Driver**: TB6612FNG Motor Driver.  
  `![Motor Driver](media/motor_driver.jpg)`
- **Drivetrain**: LEGO differential with custom 3D-printed gear.

### Steering

- **Type**: Parallelogram front-wheel steering.
- **Servo**: MG90S Micro Servo.  
  `![MG90S Servo](media/mg90s_servo.jpg)`
- **Turn Angle**: Up to ±50 degrees for sharp cornering.
- **Mounts**: Carbon fiber rods with custom joints.

---

## 🛠️ Power & Sensors

### Power Supply

- **Battery**: 3S 450mAh Li-Po.  
  `![Li-Po Battery](media/lipo_battery.jpg)`
- **Regulator**: L7805CV Linear Regulator.  
  `![Voltage Regulator](media/voltage_regulator.jpg)`

### Main Controller

- **Board**: Arduino Nano ESP32 (handles sensors & motors).  
  `![Arduino Nano ESP32](media/arduino_esp32.jpg)`

### Vision

- **Camera**: OpenMV H7 (detects traffic signs, lanes).  
  `![OpenMV Camera](media/openmv_h7.jpg)`

### Sensors

- **IMU**: BMI088 (gyro + accelerometer).  
  `![BMI088 IMU](media/bmi088.jpg)`
- **Distance**: JS40F IR Sensor (parking & obstacle detection).  
  `![JS40F Sensor](media/js40f.jpg)`

---

## 🔧 Assembly & Testing

### Steps

1. 3D Print parts and test fit.
2. Assemble drivetrain and steering.
3. Solder PCB and mount it.
4. Install sensors, motor, battery.
5. Secure all wiring and connectors.
6. Upload code to Arduino and OpenMV.

_Add Wiring Diagram:_  
`![Wiring Diagram](media/wiring_diagram.jpg)`

### Testing

- Lane tracking in controlled lighting.
- Obstacle avoidance using color detection.
- Parking maneuver tested on scale layout.

---

## 🔎 Obstacle Handling

### OpenMV H7 Logic

- Detects red (R) and green (G) cubes.
- Sends UART command to Arduino for avoidance.

### Arduino Logic

- Implements a finite state machine:
  - **PID**: Straight line using gyro.
  - **FOLLOW_CUBE**: Camera directs servo.
  - **AVOID_CUBE**: Turns + moves based on cube color.
  - **AFTER_CUBE**: Recenters after avoidance.

### Parking Logic

- Determines parking side from lap direction.
- Executes 2-step parallel park using gyro-based turns.

_Add Image of Robot During Parking:_  
`![Parking Demo](media/parking_demo.jpg)`

---

## 📉 Cost Breakdown

| Component                 | Qty | Unit Cost (₹) | Total (₹) |
| ------------------------- | --- | ------------- | --------- |
| Raspberry Pi HDMI         | 1   | 1800          | 1800      |
| Camera Module 3 Wide      | 1   | 1800          | 1800      |
| PCA9685 Servo Motor Driver| 1   | 400           | 400       |
| Switch                    | 1   | 6500          | 6500      |
| tb6612Fng Motor Driver    | 1   | 700           | 700       |
| MG995 Servo Motor         | 1   | 1000          | 1000      |
| N20 Motors                | 2   | 300           | 300       |
| Ambrane 10,000 MAh 33W
  Power Bank                | 1   | 600           | 600       |
| LiPo 18650 battery        | 1   | 500           | 500       |
| LiDAR                     | 1   | 500           | 500       |
| 3D Printed Parts          | -   | 1500          | 1500      |
| Misc. (wires, nuts, glue) | -   | 500           | 500       |
| **Total**                 |     |               | **16600** |

