# GMOS MOS Spatial Offsets

The telescope offsets executed over the course of the sequence. Unlike a long-slit or IFU
configuration, a MOS mask has no single slit to nod along — each target sits in its own slit cut
into the mask — so the positions are a plain, numbered list rather than an along-slit/to-sky pair.

There is only one preset, **Default**, since there is no instrument-standard nod pattern for an
arbitrary mask layout. Once you hand-edit the list away from it, the dropdown shows **Custom**,
and a revert icon appears to restore the default.

Each position has its own offset (in arcsec) and a guiding toggle for whether the guider stays
locked while that position executes. Use the ✚ button to add another position and the trash icon
to remove one; the first position cannot be removed.
