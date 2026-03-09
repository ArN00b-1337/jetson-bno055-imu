Jetson Orin NX + BNO055 IMU Interface

"Platform" (https://img.shields.io/badge/Platform-Jetson%20Orin%20NX-green)
"Interface" (https://img.shields.io/badge/Interface-I2C-blue)
"Sensor" (https://img.shields.io/badge/Sensor-BNO055-orange)

This repository documents the hardware interfacing of a BNO055 9-DoF IMU with the NVIDIA Jetson Orin NX using the I²C interface.

---

Hardware

- NVIDIA Jetson Orin NX
- BNO055 9-DoF IMU sensor
- Jumper wires

---

Wiring

BNO055 Pin| Jetson Orin NX (40-pin header)
VIN / VCC| Pin 1 (3.3V)
GND| Pin 6 (GND)
SDA| Pin 3 (I2C1_SDA)
SCL| Pin 5 (I2C1_SCL)

---

Connection Diagram

BNO055 IMU                          Jetson Orin NX (40-pin header)

      +------------+                      +-----------------------------+
      |            |                      |                             |
VCC --| VCC        |--------------------->| Pin 1   (3.3V)              |
GND --| GND        |--------------------->| Pin 6   (GND)               |
SDA --| SDA        |--------------------->| Pin 3   (I2C1_SDA)          |
SCL --| SCL        |--------------------->| Pin 5   (I2C1_SCL)          |
      |            |                      |                             |
      +------------+                      +-----------------------------+

---

Install Dependencies

sudo apt update
sudo apt install i2c-tools
pip3 install adafruit-circuitpython-bno055 adafruit-blinka

---

Verify I²C Connection

sudo i2cdetect -y -r 1

The BNO055 should appear at address:

0x28 or 0x29

---

Example Python Usage

An example script can be written using the Adafruit BNO055 Python library to read orientation and IMU data from the sensor.

Example command:

python3 bno055_read.py

---

Notes

This repository focuses on the hardware connection and interface setup between the Jetson Orin NX and the BNO055 sensor.
Sensor data can then be accessed through Python or integrated into robotics frameworks such as ROS.
