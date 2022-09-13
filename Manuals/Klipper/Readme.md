# Software configuration and testing

## First things first
1. You need to adjust Spider serial (line 17 in printer.cfg) to match yours. 
2. The configuration is preset for 350mm, go trough the configuration and adjust it in positions where you see 250mm or 300mm variants if you have different size kit.
3. Before heating the bed for first time, make sure it is only tightened in one corner (preferably the one next to the z-endstop sensor). If you need to do any adjustments with wires afterwards but before you have finished with bed make sure to temporarily tighten the bed down for that procedure.
4. Depending on you going with Fluidd or Mainsail way, only upload one of those configs to your web interface. On the bottom of printer.cfg file you see inclusions, make sure to replace line 626 with Mainsail.cfg if your choise is not Fluidd.

### Next: [Testing your work](../Testing/Readme.md)

---
### Back: [Manuals](../Readme.md)
