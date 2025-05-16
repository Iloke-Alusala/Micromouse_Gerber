# 🐭 Micromouse Power Subsystem – UCT EEE3088F Design Project

This repository contains the KiCad schematic and PCB design files for the **power subsystem** of a modular micromouse robot, developed as part of the EEE3088F final year design course at the University of Cape Town.

---
# ⚠️ Warning: Do Not Use As-Is
This repository contains schematic and PCB design files for a micromouse power subsystem. These designs are provided for reference and educational purposes only.

Several components in the schematic and PCB do not function as intended due to design or implementation limitations, though many of the core design choices and ideas remain valid. Always check all datasheets of ICs and components used in a given section before adopting this to your own design.**

Therefore, this hardware should not be used as-is for production or critical applications.You are encouraged to use the files for inspiration or as a starting point, but please verify and test all circuits thoroughly before use in any real-world system.
---

## 📌 Project Overview

Micromouse robots are autonomous robots that solve mazes using onboard logic and control systems. This project focused on developing the **power subsystem**, a critical part of the micromouse architecture. The design was constrained by size (82mm x 60mm), budget (R600), and modularity requirements. The subsystem is responsible for:

- Supplying **regulated voltages** from the LiPo battery (3.3V and 5V)
- Enabling **bidirectional motor control**
- Charging a **single-cell LiPo battery** (200mA/600mA modes) from Type-C charging
- Providing **external load switching** for sensors and logic
- Supporting **testability** and **fault isolation**

---

## 🔧 Key Design Goals

- **Bidirectional Motor Driving** via dual DRV8833 H-Bridge ICs
- **Type C Battery Charging Support** using TP4056-MS and XL1509 buck converter, as well as the CH224K PD negotiator
- **High-Side Load Switching** through AP22966 ICs (1A per channel)
- **Modular Power Path** allowing buck and charger stages to be tested independently
- **Design-for-Testability** with test points, jumper-control pads, and 1206 resistor footprints
- **Battery Monitoring** using INA219 and I2C connection to external microcontroller
- **Regulated 5V and 3.3V ouptu voltages supporting 300mA and 1.5A outputs**
- **Physical ON-OFF switch for disabling and enabling battery connection to the board**

---

## 📁 Repository Structure
```bash
Micromouse_Power_Subsystem/
├── KiCad_Project/
├── power_subsystem.kicad_sch        # Schematic file
│  ├── power_subsystem.kicad_pcb        # PCB layout
│   ├── project.kicad_pro                # KiCad project file
│   └── gerber/                          # Output Gerber files
├── README.md
## 
