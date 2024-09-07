# Installing the gpsd-client module
```shell
sudo apt-get install gpsd gpsd-clients
```
Use `from gps import *` in your python script to access gps functions

To start gpsd server use:
`sudo gpsd /dev/serial0 -F /var/run/gpsd.sock`

Run the library_gps script:
`python3 library_gps.py`

