# Tuning the printer
1. PID_CALIBRATE HEATER=heater_bed TARGET=100
   1. This will take ~10min
   2. Once this is done, use SAVE_CONFIG
2. Enter M106 S64 <- this will turn on the part cooling fan at 25%
3. Enter PID_CALIBRATE HEATER=extruder TARGET=245
   1. Once this is done, use SAVE_CONFIG
4. Next up take a ruler and try to get gantry as even as possible on both sides.
   1. Make sure the nozzle will clear the bed
   2. G28
   3. Press QGL to start automatic leveling
      1. The probe will measure distance in all four corners and adjust is each corner automatically until all corners are adjusted. It will try up to five times before giving up.
      2. Tolerance allowed is 0.00750, if you did your assembly correctly, it should be no problem to beat.
5. Extruder
   1. Add bowden to the the toolhead
   2. Try to extrude filament, configuration is already tuned for you
6. Z-Endstop calibration
   1. Once the chamber has heated up (set extruder to 240, heat bed to 100)
   2. Add a sheet of paper between the bed and toolhead
   3. Run Z_ENDSTOP_CALIBRATE 
      1. Then run TESTZ Z=-1 untill the nozzle is close to the paper
      2. If you go too far, run a TESTZ Z=1
      3. Once you are close, switch to TESTZ Z=-0.1
      4. Do this until you feel a drag on the paper when moving it
      5. Remove the paper
      6. Beacuse we did this hot, we need to do one more TESTZ Z=-0.1
      7. ACCEPT
      8. SAVE_CONFIG
      9. The nozzle bed offset is done for now.


For configuring MainsailOS from SSH, ener SUDO raspi-config. From there you can join your device to WiFi should you choose to do so.

---
### Back: [Manuals](../Readme.md)

# Sources:
[Youtube: Voron 2.4 Step By Step Part 13 Tuning, SuperSlicer and First Print](https://youtu.be/1wBi1mXVVEQ)