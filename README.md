# 🐭 Micromouse Power Subsystem – UCT EEE3088F Final Year Project

This repository contains the KiCad schematic and PCB design files for the **power subsystem** of a modular micromouse robot, developed as part of the EEE3088F final year design course at the University of Cape Town.


---

## 📌 Project Overview

Micromouse robots are autonomous robots that solve mazes using onboard logic and control systems. This project focused on developing the **power subsystem**, a critical part of the micromouse architecture. The design was constrained by size (82mm x 60mm), budget (R600), and modularity requirements. The subsystem is responsible for:

- Supplying **regulated voltages** (3.3V and 5V)
- Enabling **bidirectional motor control**
- Charging a **single-cell LiPo battery** (200mA/600mA modes)
- Providing **external load switching** for sensors and logic
- Supporting **testability** and **fault isolation**

---

## 🔧 Key Features

- **Bidirectional Motor Driving** via dual DRV8833 H-Bridge ICs
- **Battery Charging Support** using TP4056-MS and XL1509 buck converter
- **High-Side Load Switching** through AP22966 ICs (1A per channel)
- **Modular Power Path** allowing buck and charger stages to be tested independently
- **Design-for-Testability** with test points, jumper-control pads, and 1206 resistor footprints

---

## 📁 Repository Structure

```bash
Micromouse_Power_Subsystem/
├── KiCad_Schematics/
│   ├── EEE3088F Micromouse Design.kicad_sch        # Schematic file
│   ├── EEE3088F Micromouse Design.kicad_pcb        # PCB layout
│   ├── EEE3088F Micromouse Design.kicad_pro                # KiCad project file
│   └── gerber/                          # Output Gerber files
├── README.md
