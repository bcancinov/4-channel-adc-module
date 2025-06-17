# 4 Channel ADC Module

**Version 0.1** – Prototype for revision and discussion

This repository contains the schematic and supporting documentation for the **4 Channel ADC Module** prototype built in KiCad EDA v9.0.0.

## Table of Contents

1. [Overview](#overview)
2. [Features](#features)
3. [Repository Contents](#repository-contents)
4. [Schematic](#schematic)
5. [User Manual](#user-manual)
6. [Usage](#usage)
7. [Bill of Materials](#bill-of-materials)
8. [License](#license)
9. [Author](#author)

## Overview

The 4 Channel ADC Module is a daughterboard for Trenz TE0720 modules (Zynq™ 7020) designed by NOIRLab to provide high-precision analog-to-digital conversion. It features a multi‑rail power system, low‑noise analog front‑end, high‑speed SAR ADCs, clock synchronization, and both USB-C and Ethernet interfaces.

## Features

* **Dimensions:** 162 mm × 171 mm, six‑layer impedance‑controlled PCB
* **ADC Front‑End:** Fully differential, low‑noise amplifiers (ADA4945‑1 & LTC2387‑18)
* **Clock Gen:** Si5342‑D jitter attenuator for 10 MHz sync
* **Interfaces:** USB‑C (FT2232HL), Gigabit Ethernet (RJ45)
* **Power:** 12 V VIN protection, multi‑rail DC‑DC converters & LDOs
* **Backplane:** Sync clock, start, error, power rails

* `README.md` – This file
* `BOM.csv` – Bill of Materials
* `adc_board_prot.pdf` – Complete schematic PDF
* `adc_board_prot.kicad_pro` – KiCad project file
* `*.kicad_sch` – Schematic sheets (power, clock\_gen, adc, ftdi, ethernet, connectors, converters, misc, b2b\_jb1-3, power variants)
* `*.kicad_pcb` – PCB layout file
* `*.kicad_prl`, `*.kicad_prl` – PCB drill/paper list
* `*.kicad_sym`, `lib.kicad_sym` – Symbol libraries
* `lib.pretty/` – Footprint library

Other directories:

* `sim/` – LTSpice & LTPowerCAD simulations
* `step/` – STEP model files
* `docs/` – Documentation sources
* `manual/` – User manual PDF

## Schematic

The complete schematic is available as a PDF:

* [Download the schematic (PDF)](./adc_board_prot.pdf)

For quick reference, a block‑diagram of the 4‑channel topology is shown below:

![Block Diagram of ADC Module](./images/block_diagram.png)

## User Manual

A detailed manual covering module description, power rails, front‑end design, and connectors can be found here:

* [Read the user manual (PDF)](manual/manual.pdf)

## Usage

1. Install [KiCad EDA 9.0.0](https://www.kicad.org).
2. Open **adc\_board\_prot.kicad\_pro** in KiCad.
3. Review schematic and BOM before fabrication.
4. Use the manual for detailed functional descriptions and assembly notes.

## Bill of Materials

A complete list of components and part numbers is provided in:

* `BOM.csv`

## License

This project is released under the **MIT License**.

## Author

**Braulio Cancino Vera**
NOIRLab
[braulio.cancino@noirlab.edu](mailto:braulio.cancino@noirlab.edu)
Date: June 17, 2025