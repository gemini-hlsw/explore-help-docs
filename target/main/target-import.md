# Target Import

Click the up-arrow button to upload a list of targets in csv (comma separated values) format.

Each column must have a header which may include:
* Name (required)
* RAJ2000 (HH:MM:SS.sss, equinox J2000)
* DECJ2000 (DD:MM:SS.ss, equinox J2000)
* pmRA (units = mas)
* pmDec (units = mas)
* epoch (decimal years)

If only the target name is supplied all other quantities will be retrieved from Simbad.

