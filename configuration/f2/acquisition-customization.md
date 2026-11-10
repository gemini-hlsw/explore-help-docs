# Flamingos-2 Acquisition

Before the science sequence, Flamingos-2 takes a short series of acquisition images so the observer can
place the target in the slit (long slit) or align the mask (MOS). This panel lets you change the **Filter** and
the **Exposure Mode** used for those images. Both start with defaults derived from the science configuration,
and the panel starts collapsed because most observations do not need to change them.

## Filter

The acquisition images use one of the three acquisition filters: J, H or K-short. By default the one closest in
wavelength to the science filter is used. To choose a different one, click **Customize** and then
**Advanced Customization**; a reset icon then appears beside the field to return to the default.
For an observation that is already in progress, the acquisition filter can still be changed.

## Exposure Mode

- **Long slit**: the default is a signal-to-noise of 10 at the science wavelength, and the exposure time and
  read mode are computed for your target. You can instead set a fixed exposure time.
  
- **MOS**: only a fixed exposure time is accepted (because Explore does not know the brightness of the MOS aligntment stars), with a default of 5 seconds.Choose a time that gives the
  targets used for alignment a good signal without saturating them. The read mode follows from the exposure time.

## Sequence

**Long slit.** The initial acquisition takes an image of the field, a 10-second image through the slit with the
telescope offset 10" in p, and finally an image through the slit on target, where the sequence pauses for the
observer.

Whether sky frames are added depends on the acquisition exposure time; there is no separate setting for it:

- **2 seconds** (bright targets): no sky subtraction. The target is bright enough to be seen directly against the sky.
- **> 2 seconds** (fainter targets): the image of the field and the on-target image through the slit
  are each preceded by a sky frame offset 10" in q, so that the sky can be subtracted.

With the default signal-to-noise exposure mode, the exposure time, and therefore which of these is used,
follows from the target's brightness. If you set a fixed exposure time, your time decides it.

**MOS.** The initial acquisition images the field with the mask out of the beam, plus a sky frame offset 10" in q.
The sequence then pauses while the observer measures and applies the offset, and repeats the pair through
the mask to confirm that the targets fall in their slitlets.

Additional fine adjustment steps may be taken if the observer needs them.
