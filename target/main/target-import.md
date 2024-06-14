# Target Import

Click the upload button ![upload](upload.png) to import a list of targets in csv (comma separated values) format
([example](https://raw.githubusercontent.com/gemini-hlsw/explore-help-docs/main/target/main/targets.csv)).

The file **must** have a header, and the possible parameters are listed below.
Rows that start with `#` or `//` are assumed to be comments and are ignored along with blank lines.

### Name

The target name is the only required parameter.
If only the target name is supplied all other quantities will be retrieved from Simbad.

* `NAME` or `Name` (required)

### Coordinates:

Coodinates must be in equinox J2000 and sexagesimal format.

* `RAJ2000` or `RaJ2000` (HH:MM:SS.sss)
* `DECJ2000` or `DecJ2000` (DD:MM:SS.ss)
* `EPOCH` or `Epoch` in decimal years, assumed to be 2000.0 if unspecified.

### Proper motion:

Specified in decimal milliarcseconds.

* `pmRA` or `pmRa`
* `pmDEC` or `pmDec`

### Parallax:

* `Parallax` or `parallax` in milliarcseconds.

### Brightness:

The target brightness may be specified in most broad-band filters with an optional unit.
The supported filters include:
* `u`, `g`, `r`, `i`, `z`, `U`, `B`, `V`, `R`, `I`, `Z`, `Y`, `J`, `H`, `K`, `L`, `M`, `N`, `Q`

Brightness units may be specified with a column filter_unit as necessary, e.g. `z_unit` or `V_unit`.
The supported units include:
* `Vega mag` or `Vega`
* `Vega mag/arcsec²`, `Vega mag/arcsec^2`, `Vega mag/arcsec2`, `Vega/arcsec²`, `Vega/arcsec^2`, or `Vega/arcsec2`
* `AB mag` or `AB`
* `AB mag/arcsec²`, `AB mag/arcsec^2`, `AB mag/arcsec2`, `AB/arcsec²`, `AB/arcsec^2`, or `AB/arcsec2` 
* `Jansky` or `Jy`
* `Jy/arcsec²`, `Jy/arcsec^2` or `Jy/arcsec2`

If not specified, Sloan filters are assumed to be in `AB` magnitudes, and all others in `Vega` magnitudes.

