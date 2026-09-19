# AUDIO5822

**Embedded audio amplifier platform based on the TAS5822 Class-D amplifier, designed for embedded audio systems using platforms such as ESP32 and ESP32-S3.**

## Overview

AUDIO5822 is a compact mono Class-D audio amplifier platform built around the **Texas Instruments TAS5822** and configured for **MONO (PBTL)** operation.

The project was developed with embedded audio applications in mind, particularly systems based on the ESP32 family and other digital platforms capable of providing compatible I²C and I²S control/data interfaces.

The repository contains the complete hardware design, PCB manufacturing files, 3D resources, technical documentation, and firmware-related material associated with the platform.

## Design Environment

The complete **AUDIO5822 hardware design** was developed using **EasyEDA** as the primary hardware design environment.

The complete hardware development workflow was carried out within the EasyEDA environment, including:

* Schematic capture and electrical design
* PCB layout and routing
* 4-layer PCB stack-up definition
* Component placement
* Design Rule Check (DRC)
* PCB visualization and 3D inspection
* Manufacturing output generation
* Bill of Materials (BOM) generation
* Pick and Place file generation
* 3D model export

The corresponding EasyEDA source files and exported hardware files are included in the repository, allowing the design to be inspected, reproduced, and further developed.

**Design Environment:** EasyEDA
**PCB:** 4-layer
**Board Dimensions:** 80.01 mm × 56.007 mm

## Key Features

* TAS5822 Class-D audio amplifier
* MONO / PBTL output configuration
* Designed for embedded audio systems
* Compatible with ESP32 and ESP32-S3 based systems
* Digital control through I²C
* Digital audio input through I²S
* 3.3 V / 1.8 V digital control and data interface compatibility
* Reverse-polarity protection on the power input
* Dedicated PVDD decoupling network
* LC output filtering
* 4-layer PCB design
* Compact PCB size: **80.01 mm × 56.007 mm**

## System Interfaces

### I²C Control

The amplifier can be configured and controlled through the **I²C interface**.

The digital interface is intended to operate with suitable **3.3 V or 1.8 V logic systems**, depending on the system implementation and interface requirements.

### I²S Audio

AUDIO5822 provides a digital audio interface suitable for embedded platforms using **I²S**.

Example target platforms include the **ESP32** and **ESP32-S3**, although the board is not limited to these devices.

## Power

* Nominal supply: **12 V**
* PVDD operating range can reach approximately **26 V**, depending on the intended TAS5822 operating conditions and system configuration.
* Mono speaker output through the TAS5822 output stage and LC filter.

> **Important:** The actual supply voltage, speaker impedance, output power, thermal conditions, and operating limits must be validated against the TAS5822 datasheet and the complete system design before operation.

## Applications

AUDIO5822 can be integrated into embedded systems such as:

* ESP32 / ESP32-S3 Bluetooth audio receivers
* Embedded speakers and audio terminals
* IoT audio devices
* Digital audio prototypes
* Custom embedded audio systems
* Microcontroller-based audio products

## Repository Structure

```text
AUDIO5822/
├── README.md
├── LICENSE
│
├── documentation/
│   └── datasheet/
│       └── AUDIO5822_Datasheet.pdf
│
├── hardware/
│   ├── schematic/
│   │   ├── AUDIO5822_Schematic.json
│   │   └── AUDIO5822_Schematic.pdf
│   │
│   ├── pcb/
│   │   ├── AUDIO5822_PCB.json  
│   │   └── AUDIO5822.obj
│   │
│   └── manufacturing/
│       ├── AUDIO5822_Gerbers.zip
│       ├── AUDIO5822_BOM.xlsx
│       └── AUDIO5822_PickAndPlace.csv
│
└── firmware/
```

## Hardware Files

### Schematic

The complete electrical schematic is provided in both source and PDF formats.

* `AUDIO5822_Schematic.json` — EasyEDA schematic source file
* `AUDIO5822_Schematic.pdf` — PDF schematic documentation

Location:

```text
hardware/schematic/
```

### PCB

The complete PCB design is provided in source, PDF, and 3D model formats.

* `AUDIO5822_PCB.json` — EasyEDA PCB source file
* `AUDIO5822_PCB.pdf` — PCB documentation
* `AUDIO5822.obj` — 3D model

Location:

```text
hardware/pcb/
```

### Manufacturing Files

The manufacturing directory contains the files required for PCB fabrication and assembly.

* `AUDIO5822_Gerbers.zip` — Gerber manufacturing files
* `AUDIO5822_BOM.xlsx` — Bill of Materials
* `AUDIO5822_PickAndPlace.csv` — Pick and Place file

Location:

```text
hardware/manufacturing/
```

## Documentation

The technical documentation provides detailed information about the AUDIO5822 hardware design, including:

* System architecture
* TAS5822 configuration
* MONO (PBTL) implementation
* Power distribution
* PVDD decoupling
* Reverse-polarity protection
* I²C and I²S interfaces
* Output LC filtering
* Bootstrap network
* PCB layout
* Component selection
* Hardware recommendations and improvements
* Applications and integration considerations

The complete technical documentation is available in the project datasheet:

**AUDIO5822 Datasheet:**
`documentation/datasheet/AUDIO5822_Datasheet.pdf`

## Project Status

**Hardware design and technical documentation completed. Repository hardware files published.**

The repository contains the main hardware source files, manufacturing outputs, 3D model, and technical documentation required to inspect and reproduce the AUDIO5822 hardware design.

Firmware examples and additional software resources may be added in future revisions.

## Author

**Juan Antonio Rodríguez Alcaraz**

Electronics Engineering · Embedded Systems · Embedded AI

GitHub: [@juanara-embedded](https://github.com/juanara-embedded)

## License

This project is released under the **MIT License**.

See [LICENSE](LICENSE) for details.

