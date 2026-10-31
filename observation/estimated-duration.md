# Remaining Estimated Duration

The time left to execute this observation, broken down into its parts.
It only ever accounts for what has not yet been observed. 
As the sequence is executed, the remaining time shrinks, and a completed observation shows zero.

|   |   |
|---|---|
| Science Sequence | The time remaining for all the exposures in the science sequence. |
| Flats & Arcs | The number of remaining calibration sets and their total time. Omitted if none remain. |
| Setup | The number of setups still expected, multiplied by the time each one takes. |
| Tellurics | The number of remaining telluric standard observations, existing and still to be generated, and their total time. Omitted if the observation uses no telluric. |
| Total | Science Sequence, Setup, any Flats & Arcs, plus the time for all tellurics. |

### Updates

These figures are calculated by the back end and can take a moment to catch up after a change to
the sequence, the targets or the instrument configuration. While that calculation is running, the
section is shown dimmed with the tooltip "Awaiting new data from server."; the last known values
stay on screen until the new ones arrive.
