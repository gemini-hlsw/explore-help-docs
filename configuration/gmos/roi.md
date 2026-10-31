# GMOS ROI

The region of interest (ROI) is the part of the GMOS detector that is read out for the science exposures, in both
imaging and spectroscopy. Reading out a smaller region is faster, which reduces overheads, but anything falling
outside it is lost. The default for all GMOS modes is **Full Frame**.

Sizes below are in unbinned pixels; at about 0.08"/pixel, 1000 pixels is roughly 80". In spectroscopy, the
dispersion (wavelength) direction runs across the three CCDs, and the spatial direction runs along the slit.

**Full Frame** - the whole detector, all three CCDs (6144 × 4224 pixels). The full imaging field, or full wavelength
coverage and the full slit length in spectroscopy.

**CCD 2** - the central CCD only (2048 × 4224 pixels), about 2.7' wide through the center of the imaging
field. Mostly used for acquisition; it is not used for spectroscopy.

**Central Spectrum** - the central 1024 rows across all three CCDs (6144 × 1024 pixels). In slit spectroscopy this gives
full wavelength coverage but only about 80" of the slit around the center, which suits long-slit observations of
compact targets.

**Central Stamp** - a small region of about 300 × 300 pixels (about 24" square) at the center of the detector,
used for acquisition images.

**Custom ROI** - user-defined regions, used mainly to read out only the pixels around MOS acquisition stars, and
occasionally to read out small science regions. Custom regions cannot yet be defined in Explore.

This field can only be changed under **Advanced Customization**. A reset icon appears beside the field once it
differs from the configuration's default, to revert back to it.
