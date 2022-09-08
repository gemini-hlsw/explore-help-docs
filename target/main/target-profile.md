# Spatial Profile

There are three options for the target spatial profile:

1. A **point** source that has a size defined by the image quality constraint and air mass (specified in the [Constraints]), the wavelength (either the central wavelength for spectroscopy or the filter for imaging). The resulting extent of the point source is reported in the ITC output.

2. A 2-dimensional **Gaussian** profile with user-defined FWHM (in arcsec), where the FWHM describes the delivered image size (i.e. it includes seeing). 

3. A **uniform** profile where the brightness is specified in surface brightness units (per arcsec^2).
