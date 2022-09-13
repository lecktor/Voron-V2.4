# Installing Fluidd

The recommended way to install Fluidd on a Raspberry Pi is to use [FluiddPi](#FluiddPi), a pre-packaged disk image. 

## FluiddPi

To install Fluidd on a Raspberry Pi:
1. Download the latest fluiddPi  [Release](https://github.com/cadriel/FluiddPI/releases)
2. Unzip the .img file from your download.
3. Use [BalenaEtcher](https://www.balena.io/etcher/) to write the .img to an 8GB (or larger) microSD card.  *THIS WILL DESTROY ALL DATA ON YOUR CARD*. 
4. If you will be using wifi, edit the file `fluiddpi-wpa-supplicant.txt` with your Wifi information. If you are having trouble seeing this file on the microSD card, try removing it and re-inserting it into your card reader.
5. Make sure that your MCU(s) is connected to your pi. If you will be using wired networking, also make sure your ethernet cable is connected.
6. Insert the microSD card into your Pi, and power on the Pi.    
7. Find your Pi on the network, and ssh into it (using PuTTY on Windows or the terminal on MacOS)
  
   The default username is `pi` and the password is `raspberry`.
    * If your network supports bonjour, the pi should show up as `fluiddpi.local`
    * If your network automatically assigns DNS hostnames, it may simply show up as `fluiddpi`
    * Failing these two options, you may need to check your router's DHCP server, and find out what IP address as been assigned to the device.
8. Connect to your Pi in a web browser: [http://fluiddpi.local](http://fluiddpi.local) (or whatever you determined the hostname/IP to be in the previous step)
9.   When you first connect, fluiddpi will ask you to "provide the moonraker API URL":  enter the same host name or IP address once more.  (`fluiddpi.local`)

### Software Update
 
As soon as you have Fluiddpi loaded, it is highly recommended that you make sure all the software is up to date.  (At times, the downloaded image file contains fairly out of date software.)

1. Access Fluidd through a web browser, using whatever IP or hostname you found above.  
(Note, you will see some errors regarding the non-configured state of your printer.  These can be ignored… for now)
2. Click the "Settings" button on the left side of the screen
3. Scroll down to the  "Software Updates" section
4. Click the "check for updates" button
5. Click "update" for each component that needs it.

### Next: [Firmware Flashing](../MCU_Firmware/Readme.md)

---
### Back: [Manuals](../Readme.md)

# Sources:
[Voron Design Wiki Fluidd](https://docs.vorondesign.com/build/software/installing_fluidd.html)  
[Fluidd](https://docs.fluidd.xyz/)