# Position Angle

The position angle describes the orientation of the field or slit(s) on the sky, measured degrees East of North, and there are 5 options supported in Explore.

* __Fixed__:
Allows setting the PA to a fixed value that will not be changed.  Use this for MOS observations.

* __Allow 180° flip__:
Allows Explore to flip the field in order to reach the best guide star. This should be used for slit spectroscopy that cannot use the average parallactic angle.

* __Average Parallactic__:
Explore will calculate the weighted average parallactic angle over the duration of the observation. This should be used for all single-target slit spectroscopy.

* __Unconstrained__:
Explore will select the PA that allows using the brightest guide star with the least amount of vignetting. This should be the preferred choice for most imaging observations.

* __Parallactic Override__:
This is for internal use by the observer if they need to make a small adjustment to the automatically calculated average parallactic angle in order to reach a guide starhtly.
