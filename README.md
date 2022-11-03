# woodmastr's Raspberry Pi Zero W 2 Setup

I run the PiZeroW2 in headless mode. So basically all installation guides are made from the terminal.

## Basic Stuff

### noip2

### GIT

### python

### RPi-GoogleDrive
This one took me quite a qhile to figure out. RPi-Googledrive gets you a live google drive directory on your pi. Go over to [rpi-Googledrive](https://github.com/programmer2514/RPi-Google-Drive).

### usbmount
usb drives are only mounted at boot time. usbmount automatically mounts usb drives under /media/usb*. install it via shell
```
sudo apt install usbmount # install usb 

```
it neads a tweak: in ```/lib/systemd/system/systemd-udevd.service ``` set ```# PrivateMounts=no``` and ```sudo reboot``` or restart systemd and udev subprocesses 
```
sudo systemctl daemon-reexec
sudo service systemd-udevd restart
```
.
### samba
### vnc headless


### Docker
Install docker and docker-compose utility via the guide on [docker site](https://docs.docker.com/engine/install/debian/#install-using-the-repository) itself.

## Web Hosting

### lemp wordpress script
Lemp for pi consists of nginx webserver, mariadb, php. Before installing nginx you might want to make sure that `apache2`is uninstalled via `sudo apt remove apache2`. Install a lemp wordpress stack with this [script](https://github.com/devskale/scripts/blob/main/lemp_wp_install.sh).

### lemp wordpress on docker
### grav cms
### ghost cms
### webmin
Webmin is a web-based interface for system administration for Unix. Using any modern web browser, you can setup user accounts, Apache, DNS, file sharing and much more. Webmin lets you manage a system from the console or remotely. Install it with

```
wget http://prdownloads.sourceforge.net/webadmin/webmin-2.000.tar.gz
tar -zxvf webmin-2.000.tar.gz
cd webmin-2.000
sudo ./setup.sh
```
and access it on standard port 10000 with eg http://raspberrypi.local:10000

## Media
### photoprism
