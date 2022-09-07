# SPIDER V2.2 MCU FW INSTALL/UPDATE

The firmware installation process for the Fysetc Spider MCU

## Prerequisites:

- Klipper must be installed onto the Raspberry Pi
- Take two blue jumpers out of the Fysetc Spider box
- You should have physical access to the MCU
- Voron Design recommends using USB to control the Spider, which simply requires connecting a USB-A to USB-C cable between the Spider and Pi. If you prefer a UART connection, please consult the fysetc documentation for the necessary configuration adjustments.


# 1. Enter DFU Mode

1.  First power off the board

2. Set jumper on 5v pin and DC5V 
![](Images\5vJumper.png)
3. Place jumper on BT0 to 3.3V pin 
![](Images\boot.png)
4. Connect USB cable to the board and RPI

5. Power up the board with 24v


# 2. Build Firmware Image

- Login to the Raspberry Pi via ssh
    ```
    username: pi
    pass: raspberry
    ```
- Run the following:
    ```
    sudo apt install make
    cd ~/klipper
    make clean
    make menuconfig
    ```
- In the menu structure there are a number of items to be selected.
    - Select “Enable extra low-level configuration options”
    - Set the micro-controller architecture is set to STMicroelectronics STM32
    - Set the Processor model to STM32F446
    - Set the Bootloader offset to 32KiB bootloader
    - If your Spider was made prior to 2021/06/23, set the Bootloader offset to 64KiB bootloader
    - Set the Clock Reference to 12 MHz crystal
    - Set the Communication interface to USB (on PA11/PA12) (note: see Fysetc documentation if you intend to use UART rather than USB)
![](Images\spider_klipper_menuconfig.png)

- Once the configuration is selected, press ```q``` to exit, and ```“Yes”``` when asked to save the configuration.

- Run the command
    ```
    make
    ```

- The make command, when completed, creates a firmware file klipper.bin which is stored in the folder /home/pi/klipper/out.

# 3. Firmware Installation

- From your ssh session, run 
    ```
    lsusb
    ```
    and find the ID of the DFU device.
- Run command below replacing 1234:5678 with the ID from the previous step 
    ```
    make flash FLASH_DEVICE=1234:5678
    ```


# 4. Exit DFU Mode

- Power off the Spider
- Remove the jumper from BT0/3.3V
- Power up the Spider
- You can confirm that the flash was successful by running
    ```
    ls /dev/serial/by-id
    ```
If the flash was successful, this should now show a klipper device, similar to:
![](Images\stm32f446_id.png)




# Sources:
https://docs.vorondesign.com/build/software/spider_klipper.html
https://wiki.fysetc.com/Spider/