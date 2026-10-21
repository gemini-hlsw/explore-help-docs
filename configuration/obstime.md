# Observation Time & Duration

**Time** sets when the observation is assumed to happen, in UTC — used to work out the target's
position and conditions, such as elevation and parallactic angle, for sequence planning and for
the elevation plot. The clock icon button sets it to the current time; if a duration is shown
below it, this also resets the duration to the sequence's full remaining time.

**Duration** lets you plan with less than the full remaining sequence, for example to see how far
a partial visit would get. It must be more than the setup time and no more than the remaining
time; values outside that range are coerced back into it. The clock-with-arrow button switches
between an explicit duration and simply using the full remaining sequence time, which is shown
alongside it when no explicit duration is set.

Both fields are read-only while more than one observation is selected, or while the sequence's
remaining time is still being recalculated.
