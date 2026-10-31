# GMOS IFU

The integral field unit (IFU) aperture used for the observation. GMOS-N and GMOS-S offer the same three choices.

**IFU-2** (IFU 2 Slits) - both pseudo-slits, giving the full 7" × 5" field. This gives the largest field but more limited
wavelength coverage. A filter is needed to keep the spectra from the two slits from overlapping on the detector.

**IFU-R** (IFU Right Slit, red) - the right half of the field only (3.5" × 5"), with extended wavelength coverage.
This is the recommended one-slit option, because the fibers in the red slit have higher and more uniform throughput
than those in the blue slit.

**IFU-B** (IFU Left Slit, blue) - the left half of the field only (3.5" × 5"), with extended wavelength coverage.

In the one-slit modes a filter may still be needed to avoid second-order contamination.

The long axis of the field rotates by 90° between the two-slit and one-slit modes, so check the position angle
after changing the IFU.

The sky is observed at the same time through a separate SKY field about 1' from the science field, so no offsets to sky are needed.

Note that the choice of IFU will changes the default presets offered under **IFU Spatial Offsets**.
The one-slit "On-source" pattern steps ±0.2" in p and ±0.5" in q; the two-slit pattern steps ±1.5" in p and ±0.9" in q.

A reset icon appears beside the field once it differs from the configuration's default, to revert back to it.

See the [GMOS components page](https://www.gemini.edu/node/10370) for the field-to-slit mapping, spectral overlap
in two-slit mode, and throughput details.
