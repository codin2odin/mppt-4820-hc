# MPPT charge controller with HS load switch and CAN

![Development Stage](https://img.shields.io/badge/development%20stage-alpha-red.svg) Development ongoing.

Schematic: [PDF file](build/mppt-4820-hc_schematic.pdf)

Bill of Materials: [CSV file](build/mppt-4820-hc_bom(hv_supply,can).csv)

Firmware repository: [charge-controller-firmware](https://github.com/codin2odin/charge-controller-firmware)

This charge controller design is modified version of [mppt-2420-hc](https://github.com/LibreSolar/mppt-2420-hc) with goal of adding support for 36v & 48v battery systems.

## Features

- Solar input terminal
    - Max. 85V (100V MOSFETs used)
    - DC/DC converter inductor current max. 20A
- Battery output terminal
    - 10 V - 60 V (supporting 12v & 24v & 36v & 48v battery systems)
    - Max. current: 20A (limited by inductor current)
- Load terminal: 20A
- New STM32G431 ARM MCU with advanced digital power conversion features
- Expandable via Olimex Universal Extension Connector (UEXT)
- Two bi-color (red/green) LEDs for status indication. Additional user interface can be included in separate PCB in front panel housing and connected via UEXT
- CAN interface via RJ45 connectors

## Mechanical design

- TO-220 MOSFETs can be screwed to large heat sink at the back
