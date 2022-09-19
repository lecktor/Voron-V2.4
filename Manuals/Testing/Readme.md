# Testing your work
1. Go to your printer management gui on web.
2. Turn on heater for extruder and set it to ***50C***. Wait for it to reach temp. Once temp is reached and it's not climbing past it, turn it off and wait for temp to go down.
3. Turn on heater for bed and set it to ***50C***. Wait for it to reach temp. Once temp is reached and it's not climbing past it, turn it off and wait for temp to go down.
4. Next up we want to test motors, for that run command:
   1. **STEPPER_BUZZ STEPPER=stepper_x** <- this causes b motor to move
   2. **STEPPER_BUZZ STEPPER=stepper_y** <- this causes a motor to move
   3. **STEPPER_BUZZ STEPPER=stepper_z** <- this is the front left corner
   4. **STEPPER_BUZZ STEPPER=stepper_z1** <- the back left corner
   5. **STEPPER_BUZZ STEPPER=stepper_z2** <- the back right corner
   6. **STEPPER_BUZZ STEPPER=stepper_z3** <- the front right corner
   7. **STEPPER_BUZZ STEPPER=extruder** <- the print head gears
5. Next up testing the end stops. Put print head in the centre of the printer.
   1. Go to Machine, refresh endstop statuses
   2. Hold down the X endstop switch, press refresh on endstop statuses
      1. It should state that it's now triggered instead of being open.
      2. Repeat steps for Y and Z endstop.
   3. Take a metal object (e.g. Caliper) and place it under the Omron proximity sensor. Press refresh on endstop statuses, it should state that it's now triggered instead of being open.
6. Testing Homing
   1. Go to console and run **G28 x** command <- the printhead will go up a little and then to the right until it hits the X endstop.
   2. Next run **G28 y** command <- the printhead will go up a little and then back until it hits the Y endstop
   3. Shut down your printer. Without moving the print head lower the gantry to bed level.
      1. Measure from the back of the bed to the centre of the print nozzel
      2. The centre of the Z endstop pin needs to be that far back from the bed.
         1. You can now fully tighten down the Z endstop.
      3. The bed needs to be moved back, so that it is ***2-3mm*** from the closest edge of the Z endstop pin.
         1. Loosen bed screws for easy moving. Tighten ***only*** screw near the Z-endstop after that.
      4. Align the print nozzle with the Z endstop on the X axis, then move the print head to the center on the Y axis.
   4. Power up your printer and send a **G28 y** command
      1. Without changing X or Y lower the gantry, until the nozzle touches the Z endstop, the nozzle should be in the centre of the pin
         1. Z endstop should be higher than the bed
   5. Testing the 0,0 location
      1. Move the print head close but not touching to the bed, in centre.
      2. Run **G28 x y** command to put the print head in the back right corner.
      3. Using Controls from UI, move the print head close to the front left corner
      4. Once you are close, run **M114**, it will show your position
      5. Move the ammounts needed to be at 0,0
         1. You should be on the corner of the bed. It is probably a good idea it rather be in a small amount, you can change it in tuning should you feel the need for it.
   6. Finding the X, Y of the Z endstop
      1. Start with **G28 x y** command
      2. Using Controls from UI , move the print head over until it lines up with the Z endstop.
      3. Run **M114** command so we get X and Y coordinates
      4. Save the result of those coordinates to Notepad
      5. Open up printer.cfg, search for safe_z_home, on line 393 you should see coordinates. Adjust them to the previous step results.
      6. Save and apply configuration
      7. After new conf is loaded, run **G28 x y z**
   7. Testing probe accuracy
      1. Run **PROBE_ACCURACY** command <- The probe will go close down to bed 10 times. From results you are looking for standard deviation of less than 0.003mm.


### Next: [Tuning the printer](../Tuning/Readme.md)

---
### Back: [Manuals](../Readme.md)

# Sources:
[YouTube: Voron 2.4 Step By Step Part 12 Software, Configuration and Testing](https://youtu.be/yfRtpPPcnN8)  
[Voron Design Docs - Initial Startup](https://docs.vorondesign.com/build/startup/)
