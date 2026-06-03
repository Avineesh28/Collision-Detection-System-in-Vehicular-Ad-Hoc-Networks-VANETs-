# Collision Detection System for Intelligent Vehicles

## Overview

The **Collision Detection System** is an embedded systems and intelligent transportation project designed to **detect vehicular accidents in real time and automatically trigger emergency response mechanisms**. By integrating **impact sensing, vehicle orientation detection, GPS-based location tracking, and GSM communication**, the system significantly reduces emergency response time and improves post-accident survival rates.

This project demonstrates applied expertise in **embedded systems, vehicular safety systems, sensor fusion, and real-time communication**, making it highly relevant for **IoT, automotive electronics, VANETs, and embedded engineering portfolios**.

---

## Objectives

- Detect vehicle collisions and rollovers automatically  
- Identify the precise geographic location of an accident  
- Notify emergency services and predefined contacts instantly  
- Improve post-accident response time and passenger safety  

---

## System Description

The system continuously monitors vehicle status using an **impact sensor** and an **ADXL335 accelerometer**. Upon detecting a collision or vehicle flip, the system retrieves the current coordinates using a **GPS module** and sends an emergency alert via a **GSM module**.

An **Arduino microcontroller** acts as the central processing unit, integrating sensor data, executing decision logic, and coordinating communication between modules. A buzzer provides immediate feedback to passengers when an emergency alert is sent.

---

## Components Used

- **Impact Sensor:** Detects physical collisions on the vehicle bumper  
- **ADXL335 Accelerometer:** Measures 3-axis acceleration to determine vehicle orientation and rollover events  
- **Arduino Microcontroller:** Processes sensor data and controls system logic  
- **GPS Module:** Determines real-time geographic location of the vehicle  
- **GSM Module:** Sends emergency alerts via SMS to contacts and emergency services  
- **Buzzer:** Audible alert for passengers  
- **Power Supply:**  
  - 5V: GSM module and impact sensor  
  - 3.3V: GPS module and ADXL335  

![Components Used](https://github.com/Avineesh28/Collision-Detection-System-in-Vehicular-Ad-Hoc-Networks-VANETs-/assets/79737929/660981c5-4baa-4b3e-ae74-e11435a25d8e)

---

## Design Overview

The system was simulated using **Proteus**:

- Impact sensor behavior simulated using a **TouchPad tool**
- ADXL335 emulated using **three potentiometers**
- GSM module programmed to transmit alert messages
- Arduino processes sensor inputs and sends location data to GSM

![Circuit Design](https://github.com/Avineesh28/Collision-Detection-System-in-Vehicular-Ad-Hoc-Networks-VANETs-/assets/79737929/8eedf11f-74ca-4a3c-843d-e36e423d3def)

![Logic Flow](https://github.com/Avineesh28/Collision-Detection-System-in-Vehicular-Ad-Hoc-Networks-VANETs-/assets/79737929/ff1b8822-37c9-4f9c-bae2-50d82e009ee6)

---

## Collision Scenarios & Logic

The system evaluates four distinct scenarios:

### Case 1: No Impact, No Flip
- Normal vehicle operation  
- GPS and GSM remain inactive  

### Case 2: Impact Detected, No Flip
- GPS retrieves current location  
- GSM sends emergency alert  

### Case 3: No Impact, Flip Detected
- GPS retrieves current location  
- GSM sends emergency alert  

### Case 4: Impact and Flip Detected
- GPS retrieves location  
- GSM sends detailed emergency alert  
- Buzzer notifies passengers  

---

## Testing & Results

The system was validated through simulation and hardware testing to ensure reliable detection and communication.

![Testing Image 1](https://github.com/Avineesh28/Collision-Detection-System-in-Vehicular-Ad-Hoc-Networks-VANETs-/assets/79737929/61563777-a2c9-4dfc-bf40-3fd58c1a7aff)

![Testing Image 2](https://github.com/Avineesh28/Collision-Detection-System-in-Vehicular-Ad-Hoc-Networks-VANETs-/assets/79737929/6b35a985-3150-4a79-98c5-c501b88cd901)

![Collision Detected](https://github.com/Avineesh28/Collision-Detection-System-in-Vehicular-Ad-Hoc-Networks-VANETs-/assets/79737929/9c59bb3d-e5e0-46ca-bc53-9be43394ac05)

![Emergency Message](https://github.com/Avineesh28/Collision-Detection-System-in-Vehicular-Ad-Hoc-Networks-VANETs-/assets/79737929/d353a00d-2179-416c-b485-ecc596f0bd56)

---

## Skills Demonstrated

- Embedded Systems Design  
- Automotive Safety Systems  
- Sensor Fusion (Impact + Accelerometer)  
- GPS-Based Localization  
- GSM Communication  
- Arduino Programming  
- Real-Time Event Detection  
- Simulation Using Proteus  

---

## Why This Project Matters

This project addresses a **real-world vehicular safety challenge** by combining sensing, communication, and automation. It demonstrates how embedded intelligence can enhance **emergency response systems**, reduce human dependency, and potentially save lives in critical scenarios.

---

## Keywords (ATS Optimization)

`Embedded Systems`, `Collision Detection`, `Automotive Safety`, `Arduino`,  
`ADXL335`, `Impact Sensor`, `GPS Tracking`, `GSM Communication`,  
`Vehicular Ad Hoc Networks (VANETs)`, `IoT`, `Real-Time Systems`,  
`Emergency Response Systems`
