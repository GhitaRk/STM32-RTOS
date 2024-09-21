# RTOS on STM32 - Academic Project

## Description
This project demonstrates the implementation of a Real-Time Operating System (RTOS) on an STM32 microcontroller. The objective is to showcase task management, scheduling, and other RTOS functionalities like semaphore handling, task delays, and hardware interfacing using FreeRTOS on the STM32 platform.

The project targets the **STM32F4xx** series microcontroller and is implemented using **FreeRTOS** for task management. The firmware includes essential initialization routines, hardware drivers, and RTOS task definitions.

## Features
- **Multi-tasking**: RTOS-based task management (e.g., task switching, scheduling)
- **Hardware abstraction**: Drivers and initialization for on-chip peripherals
- **Inter-task communication**: Semaphore/mutex handling (if applicable)
- **Peripheral control**: GPIO, UART, or other peripherals interfaced via RTOS tasks

## Hardware and Software Requirements
- **Microcontroller**: STM32F4 series (STM32F407 or similar)
- **IDE**: STM32CubeIDE or Keil uVision
- **RTOS**: FreeRTOS
- **Programming Language**: C

## Installation

1. **Clone the repository**:
    ```bash
    git clone <repository-url>
    ```

2. **Open the project** in STM32CubeIDE or Keil uVision.

3. **Connect the STM32 board** via ST-Link or USB for programming and debugging.

4. **Compile and Flash** the program to the STM32 microcontroller.

## Requirements
- **STM32CubeMX**: For generating HAL drivers and initial project setup.
- **STM32CubeIDE** or **Keil**: For writing and debugging the project.
- **FreeRTOS**: The RTOS kernel that handles task scheduling.

### Files Overview

#### main.c
The `main.c` file is the entry point of the project. It initializes the hardware and starts the RTOS scheduler. It contains:
- System clock configuration
- Hardware initialization (GPIO, UART, etc.)
- Task creation and initialization
- RTOS kernel startup

#### finalize_hardware_init.c
This file handles the detailed initialization of hardware peripherals. It ensures that all connected devices and onboard peripherals are correctly set up before entering the main application loop. Functions in this file include:
- GPIO initialization
- UART configuration
- Any necessary peripheral setups like ADC, I2C, SPI, etc.
