# F2 MOS Spatial Offsets

The telescope offsets executed over the course of the sequence, as two lists: positions along the
slits, and positions off the mask entirely, on blank sky. Offsetting along the slits moves each
target to different points along its slit between exposures; offsetting to sky moves the
telescope away from the mask altogether so that sky background can be measured.

Choose a named preset from the dropdown — **Sparse field** or **Crowded field** — to set both
lists at once to the pattern suited to how densely the mask's slits are packed with targets. Once
you hand-edit a list away from the active preset's pattern, the dropdown shows **Custom**, and a
revert icon appears to restore the default.

Each position in the along-slit list has only an along-slit offset; each position in the to-sky
list has a full telescope offset. Both kinds also have a guiding toggle for whether the guider
stays locked while that position executes. Use the ✚ button on either list to add another
position and the trash icon to remove one; the first position in a list cannot be removed.
