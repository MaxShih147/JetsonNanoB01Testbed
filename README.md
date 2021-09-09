# JetsonNanoB01Testbed

### Materials

### Fan Control
sudo sh -c 'echo 255 > /sys/devices/pwm-fan/target_pwm'

cd /etc
sudo touch rc.local
sudo chmod u+x rc.local
sudo vim rc.local

#!/bin/bash
sleep 10
sudo /usr/bin/jetson_clocks
sudo sh -c 'echo 255 > /sys/devices/pwm-fan/target_pwm'


### Python Setup
```console
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install libfreetype6-dev pkg-config -y
sudo apt-get install zlib1g-dev zip libjpeg8-dev libhdf5-dev -y
sudo apt-get install libssl-dev libffi-dev python3-dev -y
sudo apt-get install libhdf5-serial-dev hdf5-tools -y
sudo apt-get install libblas-dev liblapack-dev
sudo apt-get install  libatlas-base-dev -y
sudo apt-get install build-essential cmake libgtk-3-dev libboost-all-dev -y
sudo apt-get install nano -y
pip install matplotlib
pip install scikit-build
pip install imutils
pip install pillow
```
