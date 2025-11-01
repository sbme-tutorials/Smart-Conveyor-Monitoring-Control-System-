# Smart Conveyor Monitoring & Control System (Proteus Simulation)

## Project Overview
This project simulates a **Smart Conveyor Monitoring and Control System** using an **ARM Cortex-M microcontroller**.  
It demonstrates key embedded system functionalities such as real-time speed measurement, PWM motor control, object detection, and emergency stop handling — all visualized through a **16x2 LCD display** in **Proteus**.

---

##  System Features

### 1️⃣ Speed Measurement (Timer Capture + Function Generator)
- Simulates pulse signals using a **Function Generator**.  
- Measures the time between two **rising edges** using **Timer Input Capture mode**.  
- **No interrupts** are used for pulse edge detection.  

### 2️⃣ Motor Speed Control (Potentiometer + PWM)
- A **potentiometer** is connected to an **ADC channel**.  
- The ADC value determines the **PWM duty cycle** to control the motor speed.  
- The **motor speed percentage** is displayed on the LCD.  

### 3️⃣ Object Detection (Software-Based Edge Detection)
- Uses a simulated **IR sensor** as a digital input.  
- Implements **falling-edge detection in software** (polling only; no interrupts).  
- Each detected object increments the **object counter**, shown on the LCD.  

### 4️⃣ Emergency Stop (Interrupt-Based Button)
- A **push button** simulates the emergency stop feature.  
- The **external interrupt** detects button presses.  
- When triggered:
  - The motor stops immediately.  
  - LCD shows: `"EMERGENCY STOP"`.  
- **No debouncing** is required.  

### 5️⃣ Display Interface
- A **16x2 LCD** displays:
  - Conveyor Speed  
  - Motor Speed (PWM %)  
  - Object Count  
  - Emergency Status  

---

## ⚙️ System Requirements & Components

| Component | Function |
|------------|-----------|
| ARM Cortex-M Microcontroller | Main control and processing unit |
| Function Generator | Simulates conveyor speed pulses |
| Potentiometer | Controls motor speed (via ADC) |
| DC Motor | Conveyor motor simulation |
| IR Sensor | Object detection |
| Push Button | Emergency stop interrupt |
| 16x2 LCD | Display interface |
| Proteus | Simulation environment |

---

## Deliverables

### 1.  Simulation
- **Proteus project file (.pdsprj)** with full system integration.

### 2.  Source Code
- **C language**, modular and well-documented.  
- Implements ADC, PWM, Timer Capture, LCD, and Interrupt handling.

### 3.  Report (PDF)
- Project overview  
- System block diagram  
- Explanation of each subsystem  
- Simulation screenshots  

### 4. Demonstration
- **Recorded video** showing the simulation and all system functionalities.  
- 🔗 **[Watch the Demo Video Here](https://github.com/user-attachments/assets/a957ba6e-2248-4abb-b364-6d6b64958bea)**

---

##  System Block Diagram
*(Insert diagram image here if available)*  
```plaintext
[Function Generator] --> [Timer Capture] --> [Speed Calc] --> [LCD]
[Potentiometer] ----> [ADC] --> [PWM] --> [Motor]
[IR Sensor] --> [Polling Logic] --> [Object Counter] --> [LCD]
[Button] --> [EXT Interrupt] --> [Emergency Stop Handler]
