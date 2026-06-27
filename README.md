# CS-350

## Overview
This repository contains work from CS 350, including Milestone Two (Serial Light Control Server) and the Final Project (Smart Thermostat Prototype). Both projects demonstrate embedded systems concepts on the Raspberry Pi 4, focusing on GPIO, serial communication, state machines, and hardware integration.

## 1. Milestone Two - Serial Light Control Server
**Summary**  
This script controls an LED on GPIO 18 based on commands received over the serial port (UART). It solves the problem of remote hardware control through simple text commands ("on", "off", "exit", "quit").

**Key Features**  
- Reads commands from `/dev/ttyS0` at 115200 baud using the `serial` library.  
- Uses a match-based command processor (simple state machine) to turn the LED on or off.  
- Proper GPIO setup and cleanup on exit.  


## 2. Final Project - Smart Thermostat Prototype
**Summary**  
This project built a functional smart thermostat on the Raspberry Pi. It reads temperature from a sensor, maintains a user-defined setpoint using heating or cooling modes, provides visual feedback with PWM LEDs, displays status on an LCD, and sends periodic updates over UART.
The system solves the problem of prototyping the cyber-physical logic for a smart thermostat before moving to a production cloud-connected device.

**Key Features**
- Finite state machine with OFF, HEAT, and COOL modes.
- LED indication: fade when actively heating/cooling, solid when at setpoint.
- Button input (toggle mode, adjust setpoint).
- LCD display with date/time and alternating status.
- UART output every 30 seconds (comma-delimited status string).
- TEST_MODE for development without the physical temperature sensor.
