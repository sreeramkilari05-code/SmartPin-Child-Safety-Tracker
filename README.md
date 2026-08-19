# SmartPin – Child Safety & Emergency Tracking System

SmartPin is an IoT-based prototype designed to improve child safety during
school transportation and movement within school facilities.

The system combines RFID-based student identification, ESP32-based emergency
handling, ESP8266 classroom nodes, smartphone-based GPS acquisition, and
Wi-Fi communication.

## Project Status

🚧 Prototype / In Development

The current implementation demonstrates the core hardware and communication
architecture on a breadboard.

## Features

- RFID-based student identification
- ESP32 as the main SmartPin controller
- ESP8266-based classroom/location nodes
- Classroom identification through nearby nodes
- SOS emergency button
- Emergency buzzer
- Emergency LED indication
- Smartphone GPS integration
- Wi-Fi communication
- HTTP-based communication between devices
- Serial monitoring for system status and GPS data

## System Architecture

```text
                    SMARTPIN
                       |
                     ESP32
                       |
        +--------------+--------------+
        |              |              |
       RFID           SOS            Wi-Fi
        |              |              |
   Student ID      Buzzer + LED       |
   Student Name                        |
                                       |
                         +-------------+-------------+
                         |                           |
                    ESP8266 Node 1             ESP8266 Node 2
                    Classroom 1                Classroom 2
                         |                           |
                         +-------------+-------------+
                                       |
                                 Location Data


                    Smartphone
                        |
                     GPS Data
                        |
                     Automate
                        |
                       Wi-Fi
                        |
                      ESP32
