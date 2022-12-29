# Target Import

Click the upload button ![upload](upload.png) to import a list of targets in csv (comma separated values) format
([example](https://github.com/gemini-hlsw/explore-help-docs/blob/main/target/main/targets.csv)).

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

Specified in decimal milliseconds.

* `pmRA` or `pmRa`
* `pmDEC` or `pmDec`

### Brightness:

The target brightness may be specified in most broad-band filters with an optional unit.
The supported filters include:
* `u`, `g`, `r`, `i`, `z`, `U`, `B`, `V`, `R`, `I`, `Z`, `Y`, `J`, `H`, `K`, `L`, `M`, `N`, `Q`

Brightness units may be specified with a column filter_unit as necessary, e.g. `z_unit` or `V_unit`.
The supported units include:
* `Vega mag` or `Vega`
* `Vega mag/arcsec²` or `Vega/arcsec²`
* `AB mag` or `AB`
* `AB mag/arcsec²` or `AB/arcsec²`
* `Jansky` or `Jy`
* `Jy/arcsec²`

If not specified, Sloan filters are assumed to be in `AB` magnitudes, and all others in `Vega` magnitudes.

