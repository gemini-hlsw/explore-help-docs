# Offset Variant

How this imaging sequence is organized across its dither offsets and, where used, its sky
offsets.

| Variant | What it adds |
|---|---|
| Grouped | A **Wavelength Order** (increasing or decreasing) for how filters are sequenced, in addition to the offsets and sky offsets common to Grouped and Interleaved. |
| Interleaved | The offsets and sky offsets pattern, without a wavelength order. |
| Pre-Imaging | Four fixed offsets (in arcsec), used instead of a generated pattern. |

Switching variant keeps the offsets pattern where the two variants share one (Grouped and
Interleaved); switching to or from Pre-Imaging replaces it with that variant's own fields instead.

For Grouped and Interleaved, see **Offsets** and **Sky Offset Count** for how the dither and sky
patterns themselves are set.
