# GMOS ROI

The region of interest: how much of the detector is read out.

| Region | Covers |
|---|---|
| Full Frame Readout | The entire detector. |
| CCD 2 | The central CCD only. |
| Central Spectrum | A narrow strip around the spectrum, for spectroscopy. |
| Central Stamp | A small box around the target, for imaging or acquisition. |
| Custom | A region not covered by the other options. |

Reading out less of the detector reduces the time spent on readout between exposures, at the cost
of not recording anything outside the chosen region.

A reset icon appears beside the field once it differs from the configuration's default, to
revert back to it.
