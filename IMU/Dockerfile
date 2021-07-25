# arm32v6 is sadly only alpine-based, needs to be debian-based.
FROM arm32v5/python:3.9-slim-buster

# Needs gcc to build RPi.GPIO
RUN apt-get update && apt-get install gcc build-essential i2c-tools python-smbus python3-rpi.gpio -y

RUN pip3 install RPi.GPIO
RUN pip3 install smbus
RUN pip3 install flask

ADD ./IMU/*.py /app/

ENTRYPOINT [ "python3", "/app/IMUServer.py" ]