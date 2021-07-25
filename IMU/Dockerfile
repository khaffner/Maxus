# arm32v6 is sadly only alpine-based, needs to be debian-based.
FROM arm32v5/python:3.9-slim-buster

# Needs gcc to build RPi.GPIO
RUN apt-get update && apt-get install gcc build-essential i2c-tools python-smbus python3-rpi.gpio -y

RUN pip3 install RPi.GPIO
RUN pip3 install smbus
RUN pip3 install flask

ADD ./IMU/IMUServer.py /app/IMUServer.py
ADD ./IMU/IMU.py /app/IMU.py
ADD ./IMU/LSM9DS0.py /app/LSM9DS0.py
ADD ./IMU/LSM9DS1.py /app/LSM9DS1.py
ADD ./IMU/LSM6DSL.py /app/LSM6DSL.py
ADD ./IMU/LIS3MDL.py /app/LIS3MDL.py

ENTRYPOINT [ "python3", "/app/IMUServer.py" ]