# Wavelength dithers

The wavelength dithers are a comma-separated list of wavelength offsets that are cycled through for each step of the observation.

The default dithers are:
- R150 grating: 0, +20, -20 nm
- R400 grating: 0, +8, -8 nm
- All other gratings: 0, +5, -5 nm

To disable dithering in wavelength set the wavelength dithers to "0" and every step will be at the central wavelength.

The offsets are limited such that the central wavelength + Δλ must lie within the wavelength range of the grating.
