# Remaining Estimated Duration

The time left to execute this observation's sequence, broken down into its parts. It only ever
accounts for what has not yet been observed: as the sequence is executed, the remaining time
shrinks, and a completed observation shows zero.

| Row | What it counts |
|---|---|
| Science Sequence | The time remaining for the biases, darks and science exposures in the science sequence. |
| Flats & Arcs | The number of remaining calibration sets containing a flat or an arc, and their total time. Omitted if none remain. |
| Setup | The number of setups still expected, multiplied by the time each one takes. |
| Tellurics | The number of remaining telluric standard observations, existing and still to be generated, and their total time. Omitted if the observation uses no telluric. |
| Total | Science Sequence, Setup, Tellurics and any Flats & Arcs, plus the time of tellurics already generated for this observation (shown in the tooltip as "Includes tellurics."). |

### When the numbers change

These figures are calculated by the back end and can take a moment to catch up after a change to
the sequence, the targets or the instrument configuration. While that calculation is running, the
section is shown dimmed with the tooltip "Awaiting new data from server."; the last known values
stay on screen until the new ones arrive.
