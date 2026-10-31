# F2 MOS Spatial Offsets

The telescope offsets executed over the course of the observation.

Choose a named preset from the dropdown
- **Sparse field** performs small offsets along the slit (q)
- **Crowded field** performs large (~5') unguided offsets to sky

If you choose to hand-edit a list away from the preset pattern, the dropdown shows **Custom**, and a revert icon appears to restore the default.

Each position in the along-slit list has only an along-slit offset; each position in the to-sky
list has a full telescope offset. Both kinds also have a guiding toggle for whether the guider
stays locked while that position executes. Use the ✚ button on either list to add another
position and the trash icon to remove one; the first position in a list cannot be removed.
