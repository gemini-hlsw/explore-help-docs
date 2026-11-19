# Imaging Offsets

The telescope positions (dithers) at which the science images are taken, given as offsets in p and q, in
arcseconds, from the base position.

The number of positions follows from the exposure count calculated for each filter and the
**Exposures per Offset**: one position for every Exposures per Offset exposures, rounding up.
With **Grouped**, the same pattern is repeated for each filter, so it has as many positions as the filter that
needs the most. With **Interleaved**, one pattern runs through the whole sequence, so it has as many
positions as all the filters together. In S/N mode the count comes from the exposure time calculation, so
a pattern may gain or lose positions when the target, the constraints or the exposure mode change.

Choosing a different type resets its values to the defaults, which put every position at the base position.

## No Offsets

Every exposure is taken at the base position, with guiding.

## Explicit

A list of positions that you enter yourself. Click **+** to add a position and the trash icon to remove one
(the first position cannot be removed). The crosshairs icon turns guiding on or off for that position.
The positions are used in order; if more are needed than you entered, the list starts again from the first.

## Uniform

A regular grid filling the rectangle between **Corner A** and **Corner B**. The grid has roughly as many
columns per row as the rectangle's width in p is to its height in q, and it always spans exactly from one
corner to the other. The spacing along p and q is therefore similar but not necessarily equal. Positions are
filled row by row, starting from the corner with the largest p and q, so if the number of positions does not
fill the grid, the last row (lowest q) is incomplete. If both corners have the same q, the positions form a
single row in p; if they have the same p, a single column in q.

## Spiral

Positions spread evenly over a circle whose diameter is **Size**, centered on the base position.
The first position is at the center and each later one is further out, following a spiral that rotates by the
golden angle (about 137.5°) at each step, so the positions are well spread whatever their number.

## Random

Positions scattered over a square whose side is **Size**, centered on the base position. The square is divided
into a grid with at least one cell per position, each position is placed at a random point near the center
of its cell, and the order is shuffled. This avoids both clumps and a regular pattern.

The random choices for Spiral (the rotation of the spiral) and Random are fixed for the observation, so the
pattern stays the same each time the sequence is regenerated, as long as the number of positions does not change.

All generated positions (Uniform, Spiral and Random) are taken with guiding.

For blank-sky positions away from the target, see **Sky Offset Count**.
