## Available Configurations

The Available Configurations table lists all instrument configurations that meet the specified requirements.

Note that Gemini North configurations will not be listed for targets with Dec < -37° and 
Gemini South configurations will not be listed for targets with Dec > +28°.

### Table Columns

#### Time (Exposure Mode = Signal / Noise)

The time required to achive the requested signal-to-noise as estimated by the Integration Time Calculator.
This includes all overheads and takes into account the target properties, the selected constraints, 
and the details of the instrument configuration.

#### S/N (Exposure Mode = Time & Count)

The signal-to-noise ratio that will result from combining the "Time & Count" exposures.

#### λ

The central wavelength of the filter or combination of filters.

#### Δλ

The filter width.

### Multiple Targets

If there are multiple targets defined in the observation the time or S/N will be calculated using the *brightest* target
in order to avoid saturation.  We attempt to indicate the brightest target at the top right of the table ("On Target"), 
however, the brightest target is calculated for each configuration, so for targets that are very close in brightness 
the one displayed at the top right may not be correct for all configurations.

The ITC output for either target may be viewed in the ITC panel using the selector at the top.
Note that this does *not* affect the sequence generation, which always uses the brightest target.

If the Time column displays a warning symbol (triangle with exclamation point) it means that information required 
for the calculation is missing, and you may hover over the icon to get more details.
