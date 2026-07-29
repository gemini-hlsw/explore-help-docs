## IGRINS-2 SVC Images

There is no need to specify an IGRINS-2 acquisition.
However, one may optionally request Slit Viewing Camera (SVC) images of the field by checking "Enable SVC".
This will add a small (~1 minute) overhead that will be charged to your program, but it may be useful if the target morphology is unknown prior to the observation. The SVC images will be obtained *after* the target has been centered in the slit.

The default SVC exposure time is 1.63 seconds, which is the minimum.

The default offsets are:
* (0,0) ➡ Target centered in the slit (and therefore not visible in the SVC)
* (5,0) ➡ Target offset 5" perpendicular to the slit

Note that the SV Camera uses a K-short filter, but it has not been photometrically calibrated, and no additional calibrations (flat fields, darks, etc) will be provided for SVC images.
