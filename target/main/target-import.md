# Target Import

Click the upload button to import a list of targets in csv (comma separated values) format.

Each column must have a header which may include:
* Name (required)
* RAJ2000 (HH:MM:SS.sss, equinox J2000)
* DECJ2000 (DD:MM:SS.ss, equinox J2000)
* pmRA (milliarcseconds)
* pmDec (milliarcseconds)
* Epoch (decimal years)

If only the target name is supplied all other quantities will be retrieved from Simbad.
