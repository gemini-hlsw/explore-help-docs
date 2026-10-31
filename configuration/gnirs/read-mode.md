# GNIRS Read Mode

The read mode sets how the detector is read out for the science exposures. Modes with more reads have lower read
noise, but take longer to read out and therefore have a longer minimum exposure time. 
Acquisition exposures choose their own read mode.

**Auto** selects the read mode for you, as described below. This is the recommended setting.

| Read mode   | Read noise | Minimum exposure | Recommended maximum | Readout time per coadd |
|-------------|------------|------------------|---------------------|------------------------|
| Very bright | 155 e⁻     | 0.2 s            | 1 s                 | 0.19 s                 |
| Bright      | 30 e⁻      | 0.6 s            | 20 s                | 0.69 s                 |
| Faint       | 10 e⁻      | 9 s              | 60 s                | 11.14 s                |
| Very faint  | 7 e⁻       | 18 s             | none                | 22.31 s                |

**Very bright** - for acquisitions of very bright targets, or high thermal backgrounds.

**Bright** - for bright objects.

**Faint** - for faint objects.

**Very faint** - for very faint objects, with the longest exposures.

An exposure shorter than the read mode's minimum is an error. An exposure longer than the recommended maximum gives
a warning, because a lower read noise mode would normally be used instead.

In **signal-to-noise** mode, Auto lets the ITC choose the read mode:

- In spectroscopy, the ITC chooses the read mode together with the exposure time.
- In imaging, the read mode is chosen to reach the requested S/N in the least wall-clock time, including readout
  time, rather than by the exposure time rules used in time-and-count mode.

A read mode you choose yourself is used for the observation, but the ITC still chooses its own when calculating the
exposure time.

In **time-and-count** mode, the read mode you set is used, both by the ITC and for the observation. If it is left on
Auto, spectroscopy uses Very bright below 0.6 s, Bright up to 20 s, Faint up to 60 s, and Very faint above that,
and imaging uses Very bright below 0.6 s and Bright otherwise.

This field can be changed after clicking **Customize**. A reset icon appears beside the field once it differs from
Auto, to revert back to it.
