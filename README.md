
# RHEL 10 Telemetry Node (ESP32)

A small hardware monitoring project that uses an ESP32 to display real-time system statistics from a Red Hat Enterprise Linux 10 server over the local network.

## Objective

The goal is to build a practical monitoring tool while gaining experience with **Linux administration, networking, Python, REST APIs, embedded systems, and MicroPython**.

The ESP32 will retrieve telemetry such as CPU, RAM, and disk usage from the RHEL server and display it on its integrated LCD.

## Goals

* Monitor RHEL server performance from dedicated hardware
* Gain experience with ESP32 and MicroPython
* Build and deploy a Python telemetry API
* Practice Linux services with systemd and Gunicorn
* Learn to secure network services with API authentication and firewalld
* Document the project and the decisions made throughout development

## Architecture

```text
[RHEL 10 Server] <--- HTTP / API ---> [ESP32 Display]
   Telemetry API                       MicroPython
   psutil                              ST7789 LCD
   systemd                             Wi-Fi
   firewalld
```

## Tech Stack

**Server:** RHEL 10.2, Python, Flask, Gunicorn, psutil, systemd, firewalld

**ESP32:** MicroPython, Wi-Fi, SPI, ST7789 LCD
