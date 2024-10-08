# Installing the gpsd-client module
```shell
sudo apt-get install gpsd gpsd-clients
```
Use `from gps import *` in your python script to access gps functions

Setup gpsd server:
`sudo systemctl stop gpsd.socket`
`sudo gpsd /dev/ttyACM0 -F /var/run/gpsd.sock`

Check GPS Data:
`sudo gpsmon`
or
`sudo cgps -s`

Run the library_gps script (to get data via serial):
`python3 library_gps.py`

Find /dev port for GPS using:
`ls -l /dev/serial/by-id`

Example: /dev/ttyACM0

To view the data stream from the USB port:
Use screen command.
Install screen:
`sudo apt install screen`

Connect Screen to device:
`screen /dev/ttyACM0 9600`

To Exit Screen:
`CTRL+a k`

# References:
Screen: https://www.cyberciti.biz/tips/linux-screen-command-howto.html
https://maker.pro/raspberry-pi/tutorial/how-to-use-a-gps-receiver-with-raspberry-pi-4
https://maker.pro/raspberry-pi/tutorial/how-to-read-gps-data-with-python-on-a-raspberry-pi
