# Embedded UPS Controller with Web-Based HMI

This project was developed as part of the **end-of-year project** at **Sidi Mohammed Ben Abdellah University, Fez**, focusing on embedded control and power electronics. The objective was to design an embedded control system that manages a group of 4 UPS units based on real-time load measurements (amps and volts), adjusting power distribution accordingly. A custom **web-based Human-Machine Interface (HMI)**, powered by JavaScript, provides live monitoring and control of the UPS systems.

## Project Overview

The embedded control system, implemented in **C** for the **PIC 16F877A** microcontroller, manages the UPS units by measuring electrical parameters such as current and voltage. Based on the load power demand, the system determines which UPS units to activate. A web interface allows users to monitor power consumption and UPS status in real time.

### Key Features
- **Real-Time Monitoring**: Continuously displays data (current, voltage, power) from the UPS systems.
- **Automated UPS Control**: Activates/deactivates UPS units based on real-time load power consumption.
- **Web-Based Interface**: Provides remote monitoring via a JavaScript-powered HMI accessible from any browser.
- **Power Data Visualization**: Graphs display live measurements and system performance.
- **Control Algorithm**: Intelligent UPS management based on load power, with a defined algorithm for activating UPS units:
  - `p < 2.6k`: **Ond_1** is active.
  - `2.6k < p < 5.2k`: **Ond_1** and **Ond_2** are active.
  - `5.2k < p < 7.85k`: **Ond_1**, **Ond_2**, and **Ond_3** are active.
  - `p > 7.85k`: All 4 UPS units (**Ond_1**, **Ond_2**, **Ond_3**, **Ond_4**) are active.

## HMI Screenshot

![HMI Screenshot](https://github.com/user-attachments/assets/3588260b-6f96-4e27-ad4a-6b4b007b1821)

*Screenshot from the "Contrôle Embarqué d'un Groupe des Onduleurs" project at Université Sidi Mohammed Ben Abdellah.*

### Instantaneous Data from the Screenshot:
- **Current**: 40.8 Amperes
- **Voltage**: 151 Volts
- **Power Consumption**: 6.15 KWatt
- **Power Graph**: Real-time power monitoring showing fluctuations and load behavior.

### UPS Status:
- **Onduleur1, Onduleur2, Onduleur3**: **On**
- **Onduleur4**: **Off**

The interface also features four buttons that indicate the status of each inverter, providing direct control over the UPS units.

## Technologies Used
- **Embedded Systems**: Developed with **C** for **PIC 16F877A** microcontroller.
- **JavaScript**: Used to create the real-time web interface.
- **Power Electronics**: Integrated with inverters to manage the UPS systems' power distribution.
- **PCB Design**: Custom PCBs designed for system integration and communication.

## How It Works
- **Embedded System**: Collects real-time electrical data and sends it to the web interface for monitoring.
- **Web Interface**: Displays live measurements and controls the UPS units via browser-based interaction.
- **UPS Management**: Controls the operation of each UPS unit depending on the power needs.

## Installation and Setup

1. **Hardware**: Connect the **PIC 16F877A** microcontroller to the UPS systems and the load.
2. **Web Interface**: Set up a web server to host the interface, making it accessible through any browser.
3. **Embedded Code**: Program the microcontroller with the provided **C** code to manage the UPS systems and send data to the interface.

## Contributing
Feel free to fork the repository and submit pull requests with improvements or bug fixes.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

For more information on my work and projects, visit my [portfolio](https://salhina.github.io/) or connect with me on [LinkedIn](https://www.linkedin.com/in/nabil-salhi).
