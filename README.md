# Jetson Orin NX + BNO055 IMU Interface

## Hardware
- NVIDIA Jetson Orin NX
- BNO055 9-DoF IMU

## Connection
BNO055 -> Jetson
VIN  -> 3.3V
GND  -> GND
SDA  -> I2C SDA
SCL  -> I2C SCL

## Install Dependencies
sudo apt install i2c-tools
pip3 install adafruit-circuitpython-bno055 adafruit-blinka

## Run
python3 bno055_read.py
