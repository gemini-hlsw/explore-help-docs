# Available Configurations

The Available Configurations table lists all instrument configurations that meet the specified requirements (mode, wavelength, spectral resolution, wavelength coverage, focal plane, focal plane size, and "special capabilities").

If the exact configuration you want is not listed, you may select a configuration that is close and used the "Advanced Configuration" to achive the desired configuration.

## Table Columns

### Time

The time required to achive the requested signal-to-noise as estimated by the Integration Time Calculator.
This includes all overheads and takes into account the target properties, the selected constraints, and the details of the instrument configuration.

If there are multiple targets defined in the observation the time will be calculated to yield the requested S/N on the *brightest* target in order to avoid saturation, and the brightest target will be indicated at the top right of the table.  The ITC output for either target may be viewed in the ITC panel using the selector at the top.

If the Time column displays a warning symbol (triangle with exclamation point) it means that information required for the calculation is missing, and you may hover over the icon to get more details.

### Slit Width & Length

The slit (or IFU) dimensions in arcseconds.

### Disperser

See the instrument web pages for additional details about each disperser:
[Flamingos2](https://www.gemini.edu/instrumentation/flamingos-2/components#Grisms),
[GNIRS](https://www.gemini.edu/instrumentation/gnirs/components#Gratings),
[GMOS](http://www.gemini.edu/instrumentation/gmos/components#Gratings),
[NIFS](https://www.gemini.edu/instrumentation/nifs/components#Gratings).

### Filter

The blocking or order-sorting filter.

### FPU

The Focal Plane Unit.

### Coverage

The wavelength coverage in microns.

### Spectral Resolution

This will either be the spectral resolution ($\Delta \lambda$), resolving power ($\lambda / \Delta \lambda$), or velocity resolution ($\Delta v$).

### Availability

The availability of the configuration.

