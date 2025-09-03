# Wavelength dithers

The wavelength dithers are a comma-separated list of wavelength offsets.

The default dithers are:
- R150 grating: 0, +20, -20 nm
- R400 grating: 0, +8, -8 nm
- All other gratings: 0, +5, -5 nm

To disable dithering in wavelength set the dithers to "0" and every step will be at the central wavelength.

The amplitude of the dithers must be such that central wavelength + Δλ lies within the wavelength range of the grating.

The sequence generator will try to get exposures at every wavelength dither, and will group wavelengths up to the maximum 1 hour allowed  between taking flats and arcs.
