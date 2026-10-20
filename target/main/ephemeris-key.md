# Ephemeris Key

A non-sidereal target moves against the sky, so it has no fixed coordinates to enter. In place of
RA and Dec it carries an **ephemeris key**: the identifier used to look its position up at the
time of each observation.

The key is set when the target is created, by searching for it in
[JPL Horizons](https://ssd.jpl.nasa.gov/horizons), and is shown here read-only. To change it,
search for the target again.

The label on the field tells you where the ephemeris comes from:

| Label | Value shown |
|---|---|
| Horizons | The kind of body and its Horizons designation, for example `Comet 73P` or `Major Body 606`. Asteroids are shown as `Asteroid`, whichever Horizons designation format they use. |
| User Supplied | The identifier of an ephemeris uploaded to the observatory rather than fetched from Horizons. |
