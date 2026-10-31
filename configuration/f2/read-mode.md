# Flamingos-2 Read Mode

How the detector is read out, trading readout noise against readout time:

| Mode | Suited to | Read noise |
|---|---|---|
| Bright Object | Strong sources, short exposures | Highest |
| Medium Object | Medium sources | Medium |
| Faint Object | Weak sources, long exposures | Lowest |

Left unset, the read mode is chosen automatically from the exposure time: Bright Object for short
exposures, moving to Medium and then Faint Object as the exposure lengthens. Set it explicitly
only if the automatic choice does not suit your science; a reset icon then appears beside the
field to clear your choice and return to the automatic one.
