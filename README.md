# Raspberry Pi 4 Raspbian Desktop
![customized raspbian desktop on pi](https://github.com/link-does-mods/rpi4_rspbn_desktop/blob/main/pi_desktop.png?raw=true)

Here is what I used on my rpi desktop setup and how to set it up like I did.
### update rpi firmware (IMPORTANT)
This should be done before anyhing else is installed as this checks and makes sure your rpi is fully up-to-date. 
```
sudo apt update
sudo apt full-upgrade
sudo rpi-update
```
Once everything is completed, reboot your rpi.
### overclocking for better performance
Make sure you have some form of active cooling as the rpi gets pretty hot while overclocked.
```
sudo nano /boot/config.txt
``` 
Once inside the text file, add:
```
over_voltage=4
arm_freq=2000
```
Then reboot your rpi. If it doesn't boot, you can manually edit the config file on another pc and remove the two lines to set it back to the defaults.
### dark theme and icons
```
sudo apt install arc-theme
sudo apt install papirus-icon-theme
sudo apt install breeze-cursor-theme
```
In order to apply the theme, you need to add theme and appearence settings in the main menu. 
Once there, under wiget, set to arc dark. Under icon theme, set to papirus dark. Under mouse cursor, set to breeze. Under window border, set to arc dark. Then log off and back in or restart to apply the changes once applied in the theme menu.
### software center
This is the same as the one in all versions of Ubuntu. 
```
sudo apt install gnome-software
sudo apt install snapd
sudo apt install flatpak
sudo apt install gnome-software-plugin-flatpak gnome-software-plugin-snap
```
### visual studio code
The best ide for raspbian as it supports many programming languages natively through extensions. You can download it from the [visual studio code website](https://code.visualstudio.com/download). Make sure to select arm or arm64 under the .deb option for Linux depending on your os architecture.  
### arduino support in visual studio code
Install the PlatformIO extension in visual studio code. It supports all arduino board types as well as having code completion. More can be read on the [PlatformIO website](https://platformio.org/).
### barrier
Allows for using one mouse and keyboard beyween your pi and another pc. Similar to a kvm switch.
```
sudo apt install barrier
```
