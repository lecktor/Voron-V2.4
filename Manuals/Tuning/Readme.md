# Tuning the printer
1. **PID_CALIBRATE HEATER=heater_bed TARGET=100**
   1. This will take ~10min
   2. Once this is done, use **SAVE_CONFIG**
2. Run **M106 S64** command <- this will turn on the part cooling fan at 25%
3. Run **PID_CALIBRATE HEATER=extruder TARGET=245** command
   1. Once this is done, use **SAVE_CONFIG**
4. Next up take a ruler and try to get gantry as even as possible on both sides.
   1. Make sure the nozzle will clear the bed
   2. Run **G28** command
   3. Press QGL to start automatic leveling
      1. The probe will measure distance in all four corners and adjust is each corner automatically until all corners are adjusted. It will try up to five times before giving up.
      2. Tolerance allowed is ***0.00750***, if you did your assembly correctly, it should be no problem to beat.
5. Extruder
   1. Add bowden to the the toolhead
   2. Try to extrude filament, configuration is already tuned for you
6. Z-Endstop calibration
   1. Once the chamber has heated up (set extruder to 240, heat bed to 100)
   2. Add a sheet of paper between the bed and toolhead
   3. Run **Z_ENDSTOP_CALIBRATE** command
      1. Then run **TESTZ Z=-1** command until the nozzle is close to the paper
      2. If you go too far, run **TESTZ Z=1** command
      3. Once you are close, switch to **TESTZ Z=-0.1** command
      4. Do this until you feel a drag on the paper when moving it
      5. Remove the paper
      6. Beacuse we did this hot, we need to run one more **TESTZ Z=-0.1** command
      7. Run **ACCEPT** command
      8. Run **SAVE_CONFIG** command
      9. The nozzle bed offset is done for now.
7.  Tighten ***all*** the screws while cabin is still hot.

Thats it for tuning. You should be now ready for your first print. If you had any issues along the way, you can take a look at [very detailed tuning guide](https://github.com/AndrewEllis93/Print-Tuning-Guide) by AndrewEllis93. 

Don't have an idea what to print? Try printing a [cube](https://www.thingiverse.com/thing:5429894) and filming it for [serial request](https://www.reddit.com/r/voroncorexy/). Please read about the process in [this serial request information questions reddit thread](https://www.reddit.com/r/voroncorexy/comments/r4ggml/serial_request_information_questions/).

> **PS:** For configuring MainsailOS from SSH, enter **SUDO raspi-config**. From there you can join your device to WiFi should you choose to do so and change local network domain name.

---
### Back: [Manuals](../Readme.md)

# Sources:
[Youtube: Voron 2.4 Step By Step Part 13 Tuning, SuperSlicer and First Print](https://youtu.be/1wBi1mXVVEQ)