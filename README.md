# 4 Channel ADC Module

**Version 0.1** – Prototype for revision and discussion

This repository contains the schematic design for a **4 Channel ADC Module** developed in KiCad EDA version 9.0.0..

## Overview

The 4 Channel ADC Module is designed by NOIRLab to provide high-precision analog-to-digital conversion for scientific instrumentation. It features:
- Board dimensions: 146 × 139 mm; six-layer PCB with impedance control


- Daughter PCB module of Tren Electronic TE0720-04-62I33MA SoC module with AMD Zynq™ 7020-2I, 1 GByte DDR3L, and 8 GByte eMMC
- Minimal backplane design: synchronization clock, start, and error signals
- Four differential input channels designed for **1 MHz sample rate**, using fully differential, low-noise, low-distortion ADA4945-1 amplifiers and LTC2387-18 18-bit ADCs for high-precision conversion
- **USB-C port (USB 2.0) via FT2232HL for programming and serial communication**
- **Gigabit Ethernet connectivity via an RJ45 port with included magnetics**
- **Multi-rail power management**: input 12 V VIN (protected by TI TPS259480AYWPR eFuse 3.5 V–23 V, 12.2 mΩ, 8 A bi‑directional); external output: ±15 V



## Schematic Structure

The schematic is organized into multiple sheets:

- **Top-level** (`adc_board_prot.kicad_sch`): Power distribution, converter interconnections, FTDI, connectors, Ethernet, and miscellaneous blocks.
- **ADC Front-End** (`converters/adc_0/adc.kicad_sch`): Four-channel ADC converter schematic featuring ADA4945-1 fully differential, low-noise, low-distortion amplifiers for input buffering and anti-alias filtering; REFBUF-based reference buffering; VCM common-mode generation; and LTC2387-18 18‑bit ADCs providing differential LVDS outputs and two-line test pattern functionality.
- **FTDI Interface** (`FTDI/ftdi.kicad_sch`): FT2232HL-based USB-to-UART and JTAG/UART multiplexing.
- **Ethernet Interface** (`ethernet/ethernet.kicad_sch`): RJ45 connectors with included magnetics for network connectivity.
- **Connectors** (`connectors/b2b_jb1/`, `connectors/b2b_jb2/`, `connectors/b2b_jb3/`): Board-to-board connectors mapping to FPGA modules.
- **Power Supply** (`power/*.kicad_sch`): Multi-rail power design including 12 VIN input, 5 V, 3.3 V, 2.5 V, 4.2 V, and ±15 V rails using TI and Linear regulators.

## Usage

1. Install [KiCad EDA 9.0.0](https://www.kicad.org).
2. Open the project file `adc_board_prot.kicad_pro`.

## Bill of Materials

A complete list of components and part numbers is provided in `BOM.csv`.

## License

This project is released under the **MIT License**. See `LICENSE` for details.

## Author

**Braulio Cancino Vera**\
NOIRLab\
[braulio.cancino@noirlab.edu](mailto\:braulio.cancino@noirlab.edu)\
Date: April 18, 2025