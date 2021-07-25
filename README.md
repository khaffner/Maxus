# Maxus

The stuff that runs on the Pi in my electric van.  
Main purpose is to provide a rear view mirror, as the van does not have this. A USB camera in the rear, connected to a Raspberry Pi Zero W that runs what's in this repo.
- Motion
  - Intended to be a video surveillance system.
  - In this case, just publishes the webcam live on port 8080 in 30fps, decent resolution and mirrored.
- Home Assistant (Car Assistant?)
  - Just to have a nice web gui around the webcam stream, and possibly more stuff in the future.
  - Has a nice app for the tablet by the driver's seat.
- IMU
  - Hardware: https://ozzmaker.com/berryimu/
  - Based on https://github.com/ozzmaker/BerryIMU/tree/master/python-BerryIMU-gyro-accel-compass
  - Web server with flask, so Home Assistant can query the data