


# Embedded UPS Controller with Web-Based HMI

This project was developed as part of the **end-of-year capstone project** at **Sidi Mohammed Ben Abdellah University, Fez**, showcasing the integration of embedded systems with power electronics and real-time monitoring. It focuses on dynamically managing a group of 4 UPS units to optimize power delivery based on real-time load demands, with a **web-based Human-Machine Interface (HMI)** for efficient monitoring and control.

---

## Key Features

### Embedded System
- **Microcontroller**: Utilized **PIC 16F877A** for robust performance in embedded control applications.
- **Real-Time Measurements**:
  - **Voltage Transformer**: Measures system voltage.
  - **Current Transformer**: Measures load current.
- **Load Power Calculation**: Calculates instantaneous power using the formula: $$P = V \times I$$. (approximated for AC loads).
- **Serial Communication**: Sends measurement data and system status to a webserver.

### Control Algorithm
The system uses an intelligent algorithm to activate or deactivate UPS units based on load power demand:

| Power Range (p)      | UPS #1 (Ond_1) | UPS #2 (Ond_2) | UPS #3 (Ond_3) | UPS #4 (Ond_4) |
|-----------------------|----------------|----------------|----------------|----------------|
| **p < 2.6 kW**       | Active         | Inactive       | Inactive       | Inactive       |
| **2.6 kW ≤ p < 5.2 kW** | Active         | Active         | Inactive       | Inactive       |
| **5.2 kW ≤ p < 7.85 kW**| Active         | Active         | Active         | Inactive       |
| **p ≥ 7.85 kW**       | Active         | Active         | Active         | Active         |

### Web-Based HMI
- **User-Friendly Interface**: Displays real-time current, voltage, and power consumption.
- **Graphical Representation**: Real-time plotting of the actual load consumption, helping to visualize system performance and power trends.
- **Control Buttons**: Provides manual control of each UPS unit's status.

---

## Implementation

![HMI Screenshot](https://github.com/user-attachments/assets/3588260b-6f96-4e27-ad4a-6b4b007b1821)

### Instantaneous Data Displayed:
- **Current**: 40.8 Amperes
- **Voltage**: 151 Volts
- **Power Consumption**: 6.15 kW
- **Power Graph**: Real-time plotting of the actual load consumption, showing fluctuations in system demand.

### UPS Status Indicators:
- **Onduleur1 (UPS #1)**: **On**
- **Onduleur2 (UPS #2)**: **On**
- **Onduleur3 (UPS #3)**: **On**
- **Onduleur4 (UPS #4)**: **Off** because the load demand (**p**) is less than 7.85 kW.

---

## Technologies Used
1. **Embedded Systems**: 
   - **Microcontroller**: PIC 16F877A.
   - **C Programming**: For real-time control and communication.
2. **Power Electronics**: Voltage and current transformers for measurement, interfacing with UPS units.
3. **Serial Communication**: Transfers data to the webserver.
4. **Webserver Software**: Hosts the HMI, enabling remote interaction.
5. **JavaScript**: Drives the dynamic real-time interface for monitoring and control.

---

## How It Works
1. **Data Acquisition**:
   - Voltage and current transformers collect real-time data.
   - The microcontroller calculates the load power and determines the required UPS operation mode.
2. **Data Transmission**:
   - Real-time measurements and system statuses are sent to the webserver via serial communication.
3. **Data Visualization**:
   - The webserver processes the data and updates the HMI for user interaction.
4. **Control Execution**:
   - The microcontroller dynamically activates/deactivates UPS units based on the control algorithm.

---

## Strengths of the Project
1. **Efficiency**: Dynamically adapts to changing power demands, minimizing energy wastage.
2. **Scalability**: Can be expanded to manage more UPS units with minor modifications.
3. **User Accessibility**: Real-time monitoring and control through a simple web interface.
4. **Robust Design**: Seamless integration of hardware and software components for reliable operation.

---

## Project Details

- **Project Duration**: March 2013 - June 2013  
- **University**: Sidi Mohammed Ben Abdellah University, Fez  
- **Team Members**:
  - **Nabil Salhi**: Project Lead  
  - **3 Other Colleagues** (Total team size: 4)  

For more information: 
[![Portfolio](https://img.shields.io/badge/GitHub-Portfolio-blue?logo=github)](https://salhina.github.io/)  [![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://www.linkedin.com/in/nabil-salhi).

---
 ` <script type="text/javascript" async src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/MathJax.js?config=TeX-MML-AM_CHTML"></script>  <script type="text/javascript">  MathJax.Hub.Queue(["Typeset", MathJax.Hub]);  </script> `
