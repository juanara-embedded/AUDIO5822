# AUDIO5822

**Embedded audio amplifier platform based on the TAS5822 Class-D amplifier, designed for embedded audio systems using platforms such as ESP32 and ESP32-S3.**

## Overview

AUDIO5822 is a compact mono Class-D audio amplifier platform built around the **Texas Instruments TAS5822** and configured for **MONO (PBTL)** operation.

The project was developed with embedded audio applications in mind, particularly systems based on the ESP32 family and other digital platforms capable of providing compatible I²C and I²S control/data interfaces.

The repository contains the complete hardware design, PCB manufacturing files, 3D resources, technical documentation, and firmware-related material associated with the platform.

## Key Features

- TAS5822 Class-D audio amplifier
- MONO / PBTL output configuration
- Designed for embedded audio systems
- Compatible with ESP32 and ESP32-S3 based systems
- Digital control through I²C
- Digital audio input through I²S
- 3.3 V / 1.8 V digital control and data interface compatibility
- Reverse-polarity protection on the power input
- Dedicated PVDD decoupling network
- LC output filtering
- 4-layer PCB design
- Compact PCB size: **80.01 mm × 56.007 mm**

## Hardware

The AUDIO5822 PCB is designed with emphasis on power distribution, short high-current paths, signal integrity, and separation between the digital control interface and the power amplification section.

The layout follows the design recommendations provided for the TAS5822, with particular attention to operation in MONO (PBTL) mode.

### Main Components

| Reference | Component | Function |
|---|---|---|
| U8 | TAS5822MDCPR | Class-D audio amplifier |
| AP74700QW6-7 | Reverse-polarity protection device | Input protection |
| L | 10 µH | Output filter inductor |
| C | 680 nF | Output filter capacitor |
| C18 | 470 µF | PVDD bulk decoupling |
| C19 | 47 µF | PVDD decoupling |
| Bootstrap capacitor | 470 nF | TAS5822 bootstrap network |
| R1 | 15 kΩ | Configuration / bias network |

## System Interfaces

### I²C Control

The amplifier can be configured and controlled through the I²C interface. The digital interface is intended to operate with suitable **3.3 V or 1.8 V logic systems**, depending on the system implementation and interface requirements.

### I²S Audio

AUDIO5822 provides a digital audio interface suitable for embedded platforms using I²S. Example target platforms include the **ESP32** and **ESP32-S3**, although the board is not limited to these devices.

## Power

- Nominal supply: **12 V**
- PVDD operating range can reach approximately **26 V**, depending on the intended TAS5822 operating conditions and system configuration.
- Mono speaker output through the TAS5822 output stage and LC filter.

> **Important:** The actual supply voltage, speaker impedance, output power, thermal conditions, and operating limits must be validated against the TAS5822 datasheet and the complete system design before operation.

## Applications

AUDIO5822 can be integrated into embedded systems such as:

- ESP32 / ESP32-S3 Bluetooth audio receivers
- Embedded speakers and audio terminals
- IoT audio devices
- Digital audio prototypes
- Custom embedded audio systems
- Microcontroller-based audio products

## Repository Structure

```text
AUDIO5822/
├── README.md
├── LICENSE
│
├── hardware/
│   ├── schematic/
│   ├── pcb/
│   ├── gerbers/
│   └── 3d/
│
├── documentation/
│   └── datasheet/
│
├── firmware/
│
└── images/
    ├── pcb/
    ├── schematic/
    └── renders/
```

## Documentation

Detailed technical documentation, including the hardware architecture, control and data interfaces, protection circuitry, filtering, bootstrap network, PCB layout, and recommended hardware improvements will be available in the project documentation.

## Project Status

**Hardware design completed. Documentation and repository organization in progress.**

The repository will be updated as additional design files, manufacturing outputs, documentation, and firmware examples are added.

## Author

**Juan Antonio Rodríguez Alcaraz**

Electronics Engineering · Embedded Systems · Embedded AI

GitHub: [@juanara-embedded](https://github.com/juanara-embedded)

## License

This project is released under the **MIT License**. See [LICENSE](LICENSE) for details.
