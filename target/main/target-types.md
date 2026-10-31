# Target Types


## Target Search
UI that allows searching Simbad for sidereal targets or JPL Horizons for non-sidereal targets

## Empty Sidereal Target
Add a target that is not in Simbad



## Target of Opportunity

A Target of Opportunity (ToO) target is for an object whose position is not known in advance, such as a transient announced by a survey alert. 
You prepare the observation ahead of time using a placeholder ToO target. 
When the target becomes known you may create an observation and it will be pre-approved for execution.


## Automatic Blind Offset

A blind offset star is a nearby star used to acquire a science target that is too faint to see in the acquisition image. 
The observer first centers the blind offset star and then offsets to the science target.

When you request a blind offset star, Explore searches the Gaia DR3 catalog within 5 arcminutes of your science target. Only stars with high-quality astrometry are considered, since any error in the star's position becomes an error in the position of your target. A star must meet all of the following conditions:

- RUWE (renormalised unit weight error) below 1.4
- Astrometric excess noise below 1 mas
- Measured magnitudes in all three Gaia bands (G, BP and RP)

Up to 1,000 qualifying stars are retrieved, nearest to the target first. Stars that are too faint to ever be usable with your instrument are excluded from the search.

The positions of your science target and all candidates are corrected for proper motion to the time of the observation, so separations are measured using where the stars will actually be.

#### Estimated magnitude

Blind offset limits are set in the V band for optical instruments and the H band for infrared instruments, 
and these bands are estimated from the Gaia G magnitude and BP − RP colour.

The estimates use the photometric relations published in the Gaia DR3 documentation (section 5.5.1, "Photometric relationships with other photometric systems"). 
Each relation gives the difference between G and the target band as a polynomial in the colour x = BP − RP:

| Band | Photometric system | Relation | Valid colour range |
|---|---|---|---|
| V | Johnson-Cousins | G − V = −0.02704 + 0.01424 x − 0.2156 x² + 0.01426 x³ | −0.5 < BP − RP < 5.0 |
| H | 2MASS | G − H = −0.1048 + 2.011 x − 0.1758 x² | −0.5 < BP − RP < 2.5 |

The estimated magnitude is G minus the value of the relation. For example, a star with G = 15.00 and BP − RP = 1.00 has an estimated V of about 15.21 and an estimated H of about 13.27.

Each relation is used only strictly inside its colour range, because the polynomials stop behaving physically outside it. A star outside the range has no estimate and cannot be used:

- **V:** the range covers almost all stars, so very few candidates are lost.
- **H:** stars with BP − RP of 2.5 or more (roughly mid-M type and later) have no H estimate and will not be automatically selected.

Because these are colour-based estimates rather than measurements, they can be less accurate for stars that do not follow the average relation, such as heavily reddened or variable stars.


#### Magnitude limits

The estimated magnitude must lie between the instrument's bright and faint limits. A star exactly at a limit is rejected. The bright limits are set so the star will not saturate in the shortest acquisition exposure under the best conditions.

| Instrument | Band | Bright limit | Faint limit | Optimal |
|---|---|---|---|---|
| ‘Alopeke | V | 6.0 | 16.0 | 8.0 |
| Zorro | V | 6.0 | 16.0 | 8.0 |
| GHOST | V | 6.0 | 18.0 | 8.0 |
| GMOS-N / GMOS-S | V | 12.4 | 19.0 | 13.0 |
| Flamingos-2 | H | 13.0 | 18.0 | 14.0 |
| GNIRS | H | 12.0 | 17.0 | 13.0 |
| IGRINS-2 | H | 13.0 | 18.0 | 14.0 |

MAROON-X does not support blind offsets.

#### How the best star is chosen

Each usable star gets a score that balances how close its magnitude is to the instrument's optimal magnitude against how far it is from the science target:

**Score = √( (Δmag / 5)² + (separation / 30″)² )**

Here Δmag is the difference between the star's estimated magnitude and the optimal magnitude. Being brighter or fainter than optimal is penalized equally. The lowest score wins. One magnitude away from optimal costs the same as being 6″ farther from the target. If two stars have the same score, the closer one is chosen.

#### After selection

For the best-ranked candidates, Explore also looks up Gaia's stellar parameters (effective temperature and surface gravity). When these match a spectrum in the stellar library, that spectrum is used for the star's exposure time calculation. Otherwise a flat spectrum is assumed.

Once a blind offset star is chosen, automatic guide star selection takes it into account. Guide stars that would place the probe arm over the blind offset star are rejected, and guide stars must remain reachable when the telescope is pointed at it.




This will also allow you to step through the blind offset star options, in case the default star is not ideal.


## Blind Offset Search

## Empty Blind Offset


## Set Base Position

The **base position** is the position an observation points to. Guide star selection is also based on it. By default it is calculated from the observation's science targets, but you can set it explicitly using **Set Base Position**.

When no base position has been set, the default base position is:
- For an observation with a single target, the base is that target's position.
- For an observation with several targets, the base is the center of all the targets' positions.

Target positions are evaluated at the time of the observation, so the default base follows each target's proper motion or ephemeris.

An explicit base position replaces the default. You might set one to center the field differently from the default, for example to balance several targets within the field of view.

Keep in mind:
- **Fixed coordinates.** An explicit base position is a fixed RA and Dec. Proper motion is not applied, and it does not follow a moving target.
- **Your science targets are unchanged.** Your targets keep their own positions; only the pointing center moves.

When an explicit base position is set, AGS uses it:
- **The catalog search** is centered on the explicit base position rather than on your targets.
- **Reachability** of each candidate within the guide probe's patrol field is evaluated from the explicit base position.
- **Vignetting** is still checked against your science targets at their own positions, so guide stars that would place the probe arm over a target are rejected as usual.

Moving the base position can therefore change which guide stars are available and which one is chosen.

To return to the default base position, clear the explicit base position.
