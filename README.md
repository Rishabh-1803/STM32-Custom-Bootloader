# STM32 Custom Secure Bootloader

A custom bare-metal bootloader for the **STM32F411 (ARM Cortex-M4)** designed to support firmware updates over UART using the **YMODEM protocol**.

## Overview

This project demonstrates embedded systems concepts such as memory mapping, linker script modification, Flash memory management, vector table relocation, firmware integrity verification, and safe application handover.

The bootloader occupies the first **16 KB of Flash** and handles firmware reception, verification, and programming of the application region.

## Hardware

- **MCU:** STM32F411CEU6 (WeAct Studio Blackpill)
- **Debugger:** ST-Link V2
- **Interface:** UART
- **Protocol:** YMODEM

## Memory Map

| Region | Start Address | Size | Description |
|---|---|---|---|
| Bootloader | `0x08000000` | 16 KB | Bootloader and firmware update logic |
| Application | `0x08004000` | 496 KB | User application firmware |

## Features

- Custom bootloader and application memory layout
- Linker script modification
- Vector table relocation
- Bootloader-to-application jump
- UART-based YMODEM firmware transfer
- Flash erase and programming
- CRC32 firmware integrity verification
- Independent Watchdog (IWDG) safety mechanism

## Build & Flash

Instructions will be added upon project completion.

## Status

**In Development**
