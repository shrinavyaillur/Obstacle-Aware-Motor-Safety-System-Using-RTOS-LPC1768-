# Obstacle-Aware Motor & Safety System Using RTOS (LPC1768)

## Project Overview

Developed an **LPC1768-based real-time safety system** using **Keil RTX RTOS** to detect obstacles using an ultrasonic sensor and automatically control a DC motor. The system uses RTOS-based multitasking to perform obstacle detection, motor control, alert generation, and event logging.

## Objectives

* Detect obstacles using an ultrasonic sensor.
* Automatically stop the DC motor when an obstacle is detected.
* Provide real-time LED and buzzer alerts.
* Implement multitasking using **Keil RTX RTOS**.
* Maintain reliable and deterministic real-time operation.

## Hardware Used

* **LPC1768 ARM Cortex-M3 Microcontroller**
* **HC-SR04 Ultrasonic Sensor**
* **DC Motor**
* **LED**
* **Buzzer**

## Software / Tools Used

* **C / Embedded C**
* **Keil µVision5**
* **Keil RTX RTOS**
* **CMSIS**
* **ARM Cortex-M3**

## RTOS Tasks

The system is organized into multiple RTOS tasks:

* **Ultrasonic Task** – Measures the distance to detect obstacles.
* **Motor Task** – Controls the DC motor based on obstacle conditions.
* **Alert Task** – Activates LED and buzzer alerts.
* **Logger Task** – Maintains timestamped event information.

## Working Principle

1. The HC-SR04 ultrasonic sensor measures the distance to an object.
2. The LPC1768 processes the sensor measurement.
3. When an obstacle is detected within the defined threshold, the motor is stopped.
4. The LED and buzzer are activated to provide an alert.
5. RTOS tasks execute concurrently according to their priorities.
6. Event information is maintained through the logging mechanism.

## Key Features

* Real-time obstacle detection
* Automatic motor shutdown
* RTOS-based multitasking
* Sensor interfacing
* Motor control
* LED and buzzer alert system
* Timestamped event logging
* Deterministic task scheduling

## Results

* Successfully detected obstacles and stopped the motor.
* Provided visual and audible alerts during obstacle detection.
* Achieved an obstacle response time of **less than 10 ms**.
* Implemented reliable RTOS task scheduling.
* Maintained event information using a circular logging buffer.

## Repository Contents

* `RTX_Conf_CM.c` – RTX RTOS kernel configuration
* `startup_LPC17xx.s` – LPC17xx startup assembly file
* `system_LPC17xx.c` – LPC17xx system and clock configuration
* `course project.sct` – Keil scatter-loading configuration

## Conclusion

The project demonstrates the implementation of a **real-time embedded safety system** using the **LPC1768 ARM Cortex-M3**, **Embedded C**, and **Keil RTX RTOS**. It combines sensor interfacing, motor control, multitasking, and real-time alert mechanisms for obstacle-aware motor operation.
