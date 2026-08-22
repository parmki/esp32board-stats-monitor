RHEL 10 Telemetry Node (ESP32)
​A low-power IoT hardware monitor that fetches real-time system stats (CPU, RAM, Disk) from a Red Hat Enterprise Linux 10 server over local Wi-Fi and renders them on an Ideaspark ESP32 display.
​Features
​MicroPython Firmware: Light, fast execution on an integrated 1.14" ST7789 LCD screen.
​Production Backend: Systemd daemon running Gunicorn + Flask to serve telemetry JSON.
​Hardened Security: API Key authentication headers and firewalld rich rules restricting access strictly to the ESP32's IP address.
​Network Fail-Safe: Displays instant visual alerts for unauthorized attempts (401) or server dropouts (OFFLINE).
​Tech Stack
​Server: RHEL 10.2, Python 3, Gunicorn, Flask, psutil, systemd, firewalld
​Microcontroller: Ideaspark ESP32, MicroPython, SPI (ST7789 driver)

[ RHEL 10 Server ] <--- HTTP GET (X-API-KEY) ---> [ ESP32 Display Node ]
 (Gunicorn API)       Restricted by firewalld       (MicroPython / LCD)
