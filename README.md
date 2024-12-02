# Embedded UPS Controller with Web-Based HMI

**Project Duration**: March 2013 - June 2013  

This project was developed as part of the **end-of-year capstone project** at **Sidi Mohammed Ben Abdellah University, Fez**. It demonstrates the integration of embedded systems with power electronics and real-time monitoring. The objective was to design a system capable of managing a group of 4 UPS units by dynamically adjusting their operation based on real-time power demand. A **web-based Human-Machine Interface (HMI)** enables efficient monitoring and control.

---

## Key Features

### Embedded System
- **Microcontroller**: Utilized **PIC 16F877A** for robust performance in embedded control applications.
- **Real-Time Measurements**:
  - **Voltage Transformer**: Measures system voltage.
  - **Current Transformer**: Measures load current.
- **Load Power Calculation**: Calculates instantaneous power using \( P = V \times I \) (approximated for AC loads).
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

## Screenshot

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

## Team Members
- **Nabil Salhi**: Project Lead
- **[3 Other Colleagues]** (Total team size: 4)

For more details, visit [Nabil Salhi’s portfolio](https://salhina.github.io/) or connect on [LinkedIn](https://www.linkedin.com/in/nabil-salhi).

---

## Suggestions for Future Improvements
1. **Expand Control Logic**:
   - Introduce load forecasting or predictive algorithms for better power management.
2. **Enhanced Visualization**:
   - Add historical data storage and playback functionality to the web interface.
3. **Integrate IoT Features**:
   - Enable remote monitoring via mobile applications or cloud platforms.
4. **Hardware Optimization**:
   - Explore more advanced microcontrollers or processors for better performance and scalability.

---
