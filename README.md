# my_pizerow2_setup

# Basic Stuff

## usbmount
usb drives are only mounted at boot time. usbmount automatically mounts usb drives under /media/usb*. install it via shell
```
sudo apt install usbmount # install usb 

```
it neads a tweak: in ```/lib/systemd/system/systemd-udevd.service ``` set ```# PrivateMounts=no``` and ```sudo reboot``` or restart systemd and udev subprocesses 
```
sudo systemctl daemon-reexec
sudo service systemd-udevd restart
```.

## docker
Install docker and docker-compose utility via the guide on [docker site](https://docs.docker.com/engine/install/debian/#install-using-the-repository) itself.

Web Hosting

