## Time Accounting

The Time Accounting table provides a top-level summary of the program time accounting split into bands.

The `Prepared` row shows the sum of the estimated durations of all defined observations, without taking into account `OR` groupings.  This includes time for nighttime calibrations such as embedded arcs and flats, as well as the automatically generated spectrophotometric standards in the Calibrations group.  When a standard is associated with observations in multiple bands the time for the standard is assigned to the lowest band.

The `Used` row sums the time charged in each band.

The `Completion` row is calculated as Used / Award per band.

*The `No Band` column corresponds to observations that have an unassigned band.
