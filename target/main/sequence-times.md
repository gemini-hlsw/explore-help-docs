# Sequence Panel

## Title bar

The title bar of the Sequence panel displays three observation times:

- The **Planned** time is the total estimated time of the observation including acquisitions and calibrations.

- The **Executed** time is the time that has been charged to the program.

- The **Pending** time is the Planned time minus the Executed time.

## GCal

Some sequences include calibration steps with the [Gemini Calibration Unit](https://www.gemini.edu/observing/telescopes-and-sites/telescopes#GCAL) (GCal).
For compactness of display, the GCal configuration is concatenated into a single string with the following component order: 

Lamp, Filter, IR Shutter, Diffuser

- **Lamp**: IR High, IR Low, QH 5W/100W, Ar arc, ThAr arc, CuAr arc, Xe arc
- **Filter**: none, ND1, ND2, ND3, ND4, ND4-5, GMOS balance, NIR balance
- **IR Shutter**: Open or Closed
- **Diffuser**: visible or IR

