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
