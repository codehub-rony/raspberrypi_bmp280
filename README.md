
This repository contains the steps I took to connect the raspberryPi with a bmp280 temp, humidity and barometric sensor. 


1. enable I2C (https://learn.adafruit.com/adafruits-raspberry-pi-lesson-4-gpio-setup/configuring-i2c)
I installed latest version of raspbian. Required libraries are already installed
sudo apt-get install -y python-smbus
sudo apt-get install -y i2c-tools

2. Installing Kernel Support (with Raspi-Config) / enable the i2c controlers
run sudo raspi-config
select interface optoins --> I2C --> enable I2C interface (yes)
reboot system
verify acitivation by ls /dev/i2c*, the files should be listed

3. install python libraries:
run sudo pip3 install adafruit-circuitpython-bmp280

3. Connect BMP280 according to layout
- test whethrsudo i2cdetect -y 1


4. pip3 install board
