# Smart Water Quality Monitoring System 💧🔬

A virtual instrumentation application designed to simulate an automated municipal or industrial water quality testing and distribution system. 

This project was developed using **NI LabVIEW** for the **Instrumentation and Measurement** course at **Addis Ababa Science and Technology University (AASTU)**.

## 🎯 Project Overview
The objective of this project is to create a digital control system that monitors water purity and tank levels in real-time. The system automatically makes logic decisions to either distribute safe drinking water to residential buildings, treat the water, or drain it completely if hazardous contamination thresholds are breached.

## 📥 System Inputs (Simulated Sensors)
* **pH Sensor:** Monitors the acidity or alkalinity of the water (Range: 0-14).
* **Turbidity Sensor:** Detects water clarity and particle suspension.
* **Ultrasonic Water Level Sensor:** Checks the main storage tank's fill level.
* **Float Switch & Power Supply:** Operates the sensors and provides safe operating limits for the main pump.

## ⚙️ Subsystems & Logic Processing
Based on the system flowchart, the virtual microcontroller processes data sequentially:
1. **Tank Level Check:** Ensures the tank has sufficient water (e.g., >90%) and the float switch is active.
2. **Turbidity Check:** Classifies water clarity into safe (<5), acceptable (5-10), or dangerous (>10) levels.
3. **pH Level Check:** 
   * **6.5 - 8.5:** Safe
   * **3 - 6.5 / 8.5 - 12:** Requires Basic or Acidic Treatment
   * **0 - 3 / 12 - 14:** Hazardous (Triggers Drain)
4. **TDS (Total Dissolved Solids) Check:** Evaluates parts-per-million. If <300, it is safe to drink. Between 300-900 triggers treatment, and >900 triggers draining.

## 📤 System Outputs
* **Water Pump Activation:** Sends water to residential distribution lines (indicated by visual houses with "WATER" labels).
* **Quality Display Gauges:** Live visual dials and text displays for **TURBIDITY**, **PH STATUS** (e.g., "BASIC", "SAFE"), and **TDS**.
* **Automated Draining System:** Visual "Draining" indicators activate automatically if water is deemed unsafe.
* **Alert Signals:** Warning lights trigger if thresholds are breached.

## 🚀 How to Run the Application
1. Clone this repository to your local machine.
2. Ensure you have **NI LabVIEW** installed on your computer.
3. Open the `.vi` file included in this repository.
4. Click the **Run** arrow (or press `Ctrl + R`) on the top toolbar.
5. Interact with the Front Panel controls (Tank level slider, Turbidity slider, pH dial, and TDS dial) to test the automated logic and see when the system decides to distribute or drain the water.

## 👥 Team Members
**Addis Ababa Science and Technology University (AASTU)**  
*College of Engineering | Electro-Mechanical Engineering Department*

* **Desalegn Lulie**
