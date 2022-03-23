- RTC DS3231
- [DS3231 datasheet](https://protosupplies.com/product/ds3231-rtc-with-eeprom-module/)
- I2C module
- [C++ Code in github](https://github.com/pasquyonline/RTC-DS3231)
- [OS in github](https://github.com/rgl/rtc-i2c-ds3231-rpi)
- [Os in github old](https://github.com/skiselev/rpi_rtc_ds3231)


- [RTC in revolution pi](https://revolutionpi.com/tutorials/overview-revpi-flat/datum-und-uhrzeit-einstellen-flat/)

- [Roboeq Learn](https://roboeq.ir/blog/%d8%b1%d8%a7%d9%87-%d8%a7%d9%86%d8%af%d8%a7%d8%b2%db%8c-%d9%85%d8%a7%da%98%d9%88%d9%84-%d8%b3%d8%a7%d8%b9%d8%aa-ds3231-%d8%a8%d8%a7-%d8%a2%d8%b1%d8%af%d9%88%db%8c%d9%86%d9%88/)

Changes
---
- in file /boot/config.txt
```
dtparam=i2c_arm=on
dtoverlay=i2c-rtc,ds3231
```
- sudo apt-get install -y i2c-tools
- i2cdetect -l
- i2cdetect -y 1
- 
```
apt-get remove --purge fake-hwclock
timedatectl set-ntp false
timedatectl status
```
- reboot
```
timedatectl status
date
```
- set time `timedatectl set-time '2020-01-17 20:54:00'`
- in file `/etc/udev/rules.d/85-hwclock.rules` set KERNEL=="rtc0", RUN+="/sbin/hwclock --hctosys --utc"
