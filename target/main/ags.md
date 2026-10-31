# Automatic Guide Star (AGS) selection

When you define an observation, Explore searches the Gaia DR3 catalog around your target for possible guide stars for the selected guide probe. Only stars with reliable Gaia astrometry are considered. Stars with a renormalised unit weight error (RUWE) of 2 or higher are excluded, since a high RUWE often indicates a binary or otherwise poorly measured source. In addition, only the 100 brightest stars (Gaia G) in the search area are retrieved; in very crowded fields this may exclude some fainter candidates.

Before any checks are made, the positions of your science target and all guide star candidates are corrected for proper motion to the time of the observation. This ensures that reachability and vignetting are evaluated using where the stars will actually be, not their catalog positions.

Each candidate then goes through the checks below, and the best star that passes all of them is chosen automatically.

## 1. Brightness

A star must be bright enough to guide on, but not so bright that it saturates the wavefront sensor. The faint limit depends on the guide probe, the guide speed and your observing conditions:

**Faint limit (Gaia G) = base limit − 0.8 × FWHM − cloud extinction**

- **Base limit** depends on the probe, guide speed and sky background (see the table below).
- **FWHM** is your requested image quality converted to the guide sensor's optical wavelength.
- **Cloud extinction** is the extinction, in magnitudes, implied by your cloud constraint.

The bright (saturation) limit is 6 magnitudes brighter than the faint limit. Stars outside these limits are not considered.

| Probe | Sky background | Fast | Medium | Slow |
|---|---|---|---|---|
| GMOS / Flamingos-2 OIWFS | Darkest / Dark | 16.4 | 16.9 | 17.6 |
| | Gray | 16.3 | 16.8 | 17.5 |
| | Bright | 16.2 | 16.7 | 17.4 |
| PWFS1 | Darkest / Dark | 14.6 | 14.9 | 16.2 |
| | Gray | 14.5 | 14.8 | 16.1 |
| | Bright | 14.4 | 14.7 | 16.0 |
| PWFS2 | Darkest / Dark | 14.7 | 15.0 | 16.3 |
| | Gray | 14.6 | 14.9 | 16.2 |
| | Bright | 14.5 | 14.8 | 16.1 |

For Altair's wavefront sensor, limits are in the R band instead, taken from separate tables for natural guide star and laser guide star modes.

## 2. Guide speed and image quality

Each star is assigned the fastest guide speed its brightness allows. Slower guiding corrects less, which can affect whether your requested image quality is delivered:

- **Fast:** delivers the requested image quality.
- **Medium:** delivers it if you requested 0.6″ or worse; otherwise image quality may be degraded.
- **Slow:** delivers it if you requested 0.8″ or worse. At 0.6″, image quality may be degraded; for better image quality than that, it will be degraded.

## 3. Reachability

The star must lie within the guide probe's patrol field. If your observation includes offsets, the star must be reachable at every offset in the sequence, so the probe can keep guiding throughout.

## 4. Science field obstruction

The probe arm must not block your science target, any other science targets or a blind offset star. Stars that would place the arm over these are rejected.

## 5. Position angle

If your position angle is fixed, only that angle is tested. If it is unconstrained, angles are tested every 10°. For each star, an angle is used only if the star passes all checks at every offset at that angle.

## How the best star is chosen

Stars that pass every check are ranked by:

1. **Guide speed:** faster is preferred.
2. **Expected image quality**
3. **Vignetting:** the less the probe arm covers the science area, the better.
4. **Brightness:** brighter is preferred.

Guide speed takes priority over vignetting: a star that allows fast guiding is chosen over a slower one even if it vignettes the science area more. If you prefer less vignetting, you can select a different candidate manually.
