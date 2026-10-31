# GNIRS Read Mode

**Auto** will select the optimal read mode based on the exposure time. This is the recommended
setting.

| Mode | Suited to exposure time | Read noise |
|---|---|---|
| Very Bright | Under 0.6 s | Highest |
| Bright | Up to 20 s | High |
| Faint | Up to 60 s | Low |
| Very Faint | Over 60 s | Lowest |

Each mode reads the detector a different number of times per coadd to reach its noise level,
which is also why a longer exposure needs a lower-noise mode: it has more time available to
average the read noise down. Set a mode explicitly only if Auto does not suit your science; a
reset icon then appears beside the field to clear your choice and return to Auto.
