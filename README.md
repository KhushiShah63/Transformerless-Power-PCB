# Transformerless Power Supply PCB

A custom transformerless power supply PCB designed using KiCad to convert AC input into a regulated 5V DC output. The design includes capacitive input current limiting, bridge rectification, filtering, voltage regulation, Zener-based protection, and LED indication.

> ⚠️ **Safety Warning:** This circuit is designed for AC mains input and does not provide transformer-based galvanic isolation. It should be handled only with appropriate electrical safety precautions.

## 📌 Project Overview

This project focuses on the design of a compact transformerless AC-to-DC power supply PCB.

The circuit accepts AC input through a screw terminal, uses a capacitive current-limiting stage followed by a bridge rectifier, filters the rectified DC voltage, and regulates the output to approximately 5V using an LM7805 voltage regulator.

The complete PCB was designed using KiCad, including schematic capture, component placement, routing, PCB layout, DRC checking, and Gerber generation.

## 🔧 Tools Used

- KiCad
- Schematic Editor
- PCB Editor
- Gerber Viewer

## ⚙️ Key Features

- Transformerless AC-to-DC conversion
- Bridge rectification using 1N4007 diodes
- Capacitive input current limiting
- DC filtering using electrolytic capacitors
- Zener-based voltage protection
- 5V voltage regulation using LM7805
- LED power/status indication
- Custom PCB layout
- Gerber files generated for manufacturing

## 🧩 Components Used

| Reference | Component | Value / Part |
|---|---|---|
| J1 | AC Input Terminal | Screw Terminal |
| C1 | Capacitor | 225k/2.2µF |
| R1 | Resistor | 1MΩ |
| D1–D4 | Rectifier Diodes | 1N4007 |
| C2 | Capacitor | 0.1µF |
| C3 | Electrolytic Capacitor | 1000µF |
| D5–D6 | Zener Diodes | Zener |
| R2–R3 | Resistors | 20kΩ |
| R4 | LED Resistor | 2.2kΩ |
| D7 | LED | LED |
| U1 | Voltage Regulator | LM7805 |
| C4 | Output Capacitor | 470µF |
| J2 | DC Output Terminal | Screw Terminal |

## 🔌 Circuit / Schematic

The schematic consists of the following main stages:

### 1. AC Input & Current Limiting

The AC input is provided through the `J1` screw terminal. The input stage uses `C1` and `R1` before the rectification stage.

### 2. Bridge Rectifier

Four `1N4007` diodes (`D1–D4`) are used to form the bridge rectifier and convert the AC input into pulsating DC.

### 3. DC Filtering

`C2` and `C3` are used in the rectified DC section for filtering and smoothing the voltage.

### 4. Zener Protection

The circuit includes two Zener diodes (`D5` and `D6`) with associated resistors (`R2` and `R3`) for voltage regulation/protection in the DC section.

### 5. 5V Regulation

The filtered DC voltage is supplied to the `LM7805` regulator (`U1`), which provides a regulated 5V output.

### 6. LED Indication

`D7` provides visual indication, with `R4 = 2.2kΩ` used as the LED current-limiting resistor.

### 7. Output Filtering

`C4 = 470µF` is connected at the output side to provide additional filtering before the 5V output is delivered through `J2`.

## 🖼️ Schematic

<img width="1073" height="731" alt="image" src="https://github.com/user-attachments/assets/190178ff-446f-4f41-b0c7-8e2631579c60" />

## 🖥️ PCB Layout

<img width="1151" height="797" alt="image" src="https://github.com/user-attachments/assets/96377774-4d47-470c-aac9-750f9d4fe8e7" />

## 🧱 3D PCB View

<img width="1426" height="830" alt="image" src="https://github.com/user-attachments/assets/4ebb59d9-3b56-4629-856e-20982636aa43" />

## 📦 Gerber Files

The generated Gerber and drill files are included in the `gerber/` folder for PCB manufacturing.
