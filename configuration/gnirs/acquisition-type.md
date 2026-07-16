## GNIRS Acquisition Type

The GNIRS acquisition type determines the steps in the acquisition sequence:

- Very Bright Target: narrow-band H<sub>2</sub> filter (2.122 μm), no sky subtraction.

- Bright Target: filter closest to the science wavelength, no sky subtraction.

- Faint Target: filter closest to the science wavelength, with sky subtraction.

The target brightness is determined by running the (imaging) ITC with a requested S/N of 10.
Based on the resulting total integration time (exposure time × coadds), targets are classified as Very Bright (< 0.5 s), Bright (< 10 s), or Faint (≥ 10 s).
