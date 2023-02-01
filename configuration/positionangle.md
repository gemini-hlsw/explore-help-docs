# Position Angle

The position angle describes the orientation of the field or slit(s) on the sky, and is measured in degrees East of North.

Explore supports 5 options:

* __Fixed__:
Allows setting the PA to a fixed value that will not be changed.  Use this for MOS observations.


* __Allow 180° flip__:
Allows the field to be flipped by 180° in order to reach the best guide star. This is recommended for slit spectroscopy that cannot use the average parallactic angle.

* __Average Parallactic__:
Use the airmass-weighted average parallactic angle. This is recommended for single-target point-source slit spectroscopy.

* __Unconstrained__:
Automatically selects the PA that allows using the brightest guide star with the least amount of vignetting. This is recommended for most imaging observations.

* __Parallactic Override__:
This may be used by the observer if a small adjustment to the automatically calculated average parallactic angle is needed to reach a guide star.
