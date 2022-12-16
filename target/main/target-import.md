# Target Import

Click the upload button ![upload](upload.png) to import a list of targets in csv (comma separated values) format.

The file **must** have a header, and the possible parameters are listed below.

### Name

The target name is the only required parameter.
If only the target name is supplied all other quantities will be retrieved from Simbad.

* `Name` (required)

### Coordinates:

Coodinates are assumed to be in equinox J2000.

* `RAJ2000` (HH:MM:SS.sss)
* `DECJ2000` (DD:MM:SS.ss)
* `Epoch` (decimal years, assumed to be 2000.0 if not specified)

### Proper motion:

* `pmRA` (decimal milliarcseconds)
* `pmDec` (decimal milliarcseconds)

### Brightness:

The target brightness may be specified in most broad-band filters with an optional unit.
* Supported filters: `u`, `g`, `r`, `i`, `z`, `U`, `B`, `V`, `R`, `I`, `Z`, `Y`, `J`, `H`, `K`, `L`, `M`, `N`, `Q`

Brightness units may be specified as filter_unit as necessary, e.g. `z_unit` or `V_unit`.
* Supported units: `Vega`, `AB`, `Jy`

If not specified, Sloan filters are assumed to be in `AB` magnitudes, and all others in `Vega` magnitudes.

