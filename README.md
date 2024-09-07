# Installing the gpsd-client module
```shell
sudo apt-get install gpsd gpsd-clients
```
Use `from gps import *` in your python script to access gps functions

To start gpsd server use:
`sudo gpsd /dev/serial0 -F /var/run/gpsd.sock`

Run the library_gps script:
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
