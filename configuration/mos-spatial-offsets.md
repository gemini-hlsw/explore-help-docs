# Spatial Offsets

The telescope offsets executed over the course of the sequence: a plain, numbered list of
positions rather than the along-slit/to-sky pair used by a single-slit configuration. The IFU has
its own dedicated sky bundle built into the field of view, so the sequence does not need to nod
off to blank sky; every position in the list is an on-target pointing.

Choose a named preset from the dropdown to set the whole list at once; the presets offered depend
on which IFU slit configuration (one slit or two) is selected. Once you hand-edit the list away
from the active preset's pattern, the dropdown shows **Custom**, and a revert icon appears to
restore the instrument's default pattern.

Each position has its own offset (in arcsec) and a guiding toggle (the crosshair icon) for
whether the guider stays locked while that position executes. Use the ✚ button to add another
position and the trash icon to remove one; the first position cannot be removed.
