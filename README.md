# Embedded Controller for UPS System with Web-Based HMI

This project was developed as part of the **end-of-year project** in association with **Sidi Mohammed Ben Abdellah University, Fez**. The goal was to design and implement an embedded control system that manages a group of 4 UPS units by measuring the amps and volts of the load/station. The system turns on and off each UPS based on the power needs of the load. 

Real-time monitoring is provided via a web-based Human-Machine Interface (HMI), which is empowered by JavaScript. The board sends measurement data (amps, volts) and the status of the 4 UPS units, and plots this information in real-time on the HMI for easy visualization.

## Project Overview

This embedded control system is designed to manage multiple UPS systems, with the main functionality focusing on real-time measurement and management of power consumption. The embedded C code runs on the **PIC 16F877A** microcontroller, which collects data from the UPS units and determines whether to activate or deactivate each UPS depending on the load's power needs. The system sends this data to a JavaScript-based web interface, which displays it in real-time graphs, giving users the ability to monitor the performance of the UPS systems remotely.

## Features

- **Real-Time Monitoring**: Displays live data from the UPS system, including amps, volts, and UPS status.
- **Automatic UPS Control**: The embedded controller adjusts the UPS power based on real-time load measurements.
- **Web-Based Interface**: A JavaScript-based interface for real-time visualization of system data on any device with a browser.
- **Real-Time Graphs**: The status and measurements of the 4 UPS units are continuously updated and plotted in graphs.
- **Remote Diagnostics**: System data helps to identify performance issues, enabling efficient troubleshooting and diagnostics.

## Screenshot of the HMI

![HMI Screenshot](https://github.com/user-attachments/assets/3588260b-6f96-4e27-ad4a-6b4b007b1821)

*Above is the screenshot from the final-year project titled "Projet de Fin d'Année - Contrôle Embarqué d'un Groupe des Onduleurs // Interface Homme Machine" from Université Sidi Mohammed Ben Abdellah, Morocco.*

The interface provides real-time monitoring and control of a group of inverters, which is crucial for managing electrical systems efficiently. Key details from the screenshot include:

- **Current Measurement**: 40.8 Amperes
- **Voltage Measurement**: 151 Volts
- **Power Consumption**: 6.15 KWatt
- A graph titled **"la Puissance en temps reel"** (Power in real-time) showing power over time, with a peak around 10 Watts before dropping sharply to 0 Watts.
- **UPS Control Algorithm**:
  - `p < 2.6k`: Only **Ond_1** is active.
  - `2.6k < p < 5.2k`: **Ond_1** and **Ond_2** are active.
  - `5.2k < p < 7.85k`: **Ond_1**, **Ond_2**, and **Ond_3** are active.
  - `p > 7.85k`: All 4 UPS systems (**Ond_1**, **Ond_2**, **Ond_3**, **Ond_4**) are active.

Additionally, there are four buttons at the bottom of the interface labeled "Onduleur1," "Onduleur2," "Onduleur3," and "Onduleur4," showing the status of each inverter.

## Technologies Used

- **Embedded Systems**: Design and implementation using PIC microcontrollers.
- **PIC 16F877A**: The microcontroller used for controlling the UPS system.
- **JavaScript**: Developed the web-based Human-Machine Interface (HMI) for system interaction.
- **Power Electronics**: Integrated with inverters to manage and monitor UPS systems.
- **C**: Used for embedded programming and system control.
- **PCB Design**: Custom PCBs were developed for hardware interfacing and integration.

## Project Components

- **Embedded System**: The core of the system responsible for controlling the 4 UPS units.
- **Web-Based HMI**: A custom JavaScript-based interface that allows users to interact with the system.
- **Real-Time Data Visualization**: Graphs that display the current load measurements and UPS status.
- **Power Management**: Embedded control to turn on or off the UPS units based on the load's power requirements.

## Installation and Setup

1. **Hardware Setup**:
   - Connect the PIC 16F877A to the UPS systems and the load station.
   - Design and fabricate the necessary PCBs for the embedded hardware.

2. **Web Interface**:
   - Set up a web server to host the JavaScript-based interface.
   - Access the web interface through any device with a browser to view live data and control the UPS systems.

3. **Embedded Code**:
   - Flash the PIC microcontroller with the provided C code to control the UPS units and send data to the web interface.

## Contributing

Feel free to fork this repository and submit pull requests with improvements, bug fixes, or new features. Contributions are always welcome!

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

For more details on the development and technical implementation of this project, check out the associated documentation or contact the repository owner.

## Contact

If you have any questions or suggestions regarding the project, feel free to reach out through [LinkedIn](https://www.linkedin.com/in/yourprofile) or by opening an issue in the repository.
