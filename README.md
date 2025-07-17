# 🛠️ Engineering Journal – WRO Future Engineers 2025  
**Team Name**: Future Dynamics  
**Institution**: XYZ International School  
**Country**: India  

### 👥 Team Members

| Name            | Role                      | Responsibilities                        |
|-----------------|---------------------------|------------------------------------------|
| Arnav Ramteke   | Lead Programmer           | Software architecture, vision & control |
| Priya Sharma    | Mechanical Designer       | CAD design, chassis & drivetrain         |
| Rishi Verma     | Electrical Engineer       | Wiring, power management, sensors setup  |
| Anaya Iyer      | Documentation & Strategy  | Journal writing, testing & logistics     |

---

## 1. 📘 Introduction & Team Overview  
We are a team of four high school students passionate about robotics, automation, and solving real-world challenges. Our project for WRO Future Engineers 2025 is an autonomous electric vehicle capable of navigating lanes, detecting obstacles, and adapting to its environment using vision and sensor fusion.

---

## 2. 🧩 Challenge Description  
The 2025 Future Engineers challenge tasked teams with designing an autonomous, sensor-driven electric vehicle that can safely complete a predefined route while reacting to dynamic obstacles and road features.

---

## 3. 🎯 Requirements & Goals  
Our vehicle needed to:
- Detect and follow lanes using computer vision  
- Stop at virtual stop lines  
- Avoid both static and moving obstacles  
- Perform consistent navigation under varying lighting conditions  

Beyond these, our goals included:
- Creating a modular software stack  
- Ensuring sensor redundancy and fault tolerance  
- Achieving over 95% success in simulation and physical tests  

---

## 4. 🧠 Design Rationale

### 🔩 Mechanical Design  
Our chassis was laser-cut from lightweight acrylic with a wheelbase optimized for turns within a 1-meter radius. We used rubber-lined tires for grip and a 2-wheel differential drive for maneuverability.

### 🔌 Electrical System  
We used a 7.4V Li-ion battery pack with a voltage regulator to safely power both the Raspberry Pi and motor driver. A fuse and polarity protection were integrated.

### 📡 Sensors & Actuators  
- **Ultrasonic (HC-SR04)** – For distance sensing up to 4m  
- **IMU (MPU6050)** – To detect orientation and motion drift  
- **Raspberry Pi Camera v2** – For lane detection and stop-line detection  
Sensors were placed with minimal occlusion, aligned with the robot's heading for optimal readings.

### 🧮 Algorithms  
- Lane detection: Color masking + Hough Transform  
- Obstacle detection: Distance thresholding  
- Control: PID controller for smooth steering  
- IMU integration: Drift correction for heading  

---

## 5. 🛠️ Development Process

### 📅 Timeline  
- ✅ Research (Week 1–2)  
- ✅ Prototyping (Week 3–4)  
- ✅ Integration (Week 5–6)  
- ✅ Testing (Week 7–8)  
- ✅ Finalization (Week 9–10)  

### 🔄 Iterations  
We iterated on:
- Chassis height (reduced to lower CoG)  
- Sensor position (ultrasonic moved to center)  
- Software refactoring (modularized code for debugging)  

---

## 6. 🔧 Hardware Integration

### Components Used

| Component          | Purpose                | Model / Specs           |
|--------------------|------------------------|--------------------------|
| Raspberry Pi 4     | Processing Unit         | 4GB RAM                 |
| L298N Motor Driver | Motor Control           | Dual H-Bridge           |
| Ultrasonic Sensor  | Obstacle Detection      | HC-SR04                 |
| IMU Sensor         | Orientation Tracking    | MPU6050                 |
| Pi Camera Module   | Vision                  | 8MP, 1080p              |

### 📷 Wiring Diagram  
_Include an image or link here_  
`![Wiring Diagram](images/wiring.png)`

---

## 7. 💻 Software Architecture

### Folder Structure

