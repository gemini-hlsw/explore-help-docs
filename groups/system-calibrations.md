# Calibrations Group

The "Calibrations" group includes automatically-generated baseline calibrations.
The observations in this group are not editable and will appear (or disappear) based on the observations in the program.
The targets will be selected based on the time of the observation.


### Spectrophotometric Standards

One specphot standard star observation will be generated for each unique instrument configuration (grating, wavelength, filter, FPU, read mode, and binning).
For programs with multiple wavelength settings used to span the gaps between CCDs, only one of these wavelength settings will be taken.
Baseline relative flux calibration is a smooth function which can be interpolated across the detector gaps.
Targets are selected from the sources listed on the [GMOS spectrophotometric standard star page](https://www.gemini.edu/instrumentation/gmos/calibrations#SpectStand).
Observations are not guaranteed to be obtained the same nights as the science observations. 

### Spectroscopic Twilight Flats

One twilight observation will be generated for each unique spectroscopic instrument configuration (grating, wavelength, filter, FPU, read mode, and binning) to provide information about the slit function.
Blank fields are selected from the list of deep blank fields compiled by Jiménez-Esteban et al. ([2012 MNRAS, 427, 679](https://academic.oup.com/mnras/article/427/1/679/1033480)).
Observations are not guaranteed to be obtained the same nights as the science observations. 
