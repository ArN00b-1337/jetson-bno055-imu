Jetson Orin NX + BNO055 IMU Interface

This repository documents the hardware interfacing of a BNO055 9-DoF IMU with the NVIDIA Jetson Orin NX using the I²C interface.

---

Hardware

- NVIDIA Jetson Orin NX
- BNO055 9-DoF IMU sensor
- Jumper wires

---

Wiring

![Image alt](https://github.com/ArN00b-1337/jetson-bno055-imu/blob/9cbd30fb7ed8c78d10fbc263fdc8bae8796c970a/diagram%20main_1.jpeg)




---

Connection Flowchart

![Image alt](https://github.com/ArN00b-1337/jetson-bno055-imu/blob/2b33922b97a8d49d7e130b4e9e89bbb2baf1cf31/connection%20flowchart.jpeg)

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
