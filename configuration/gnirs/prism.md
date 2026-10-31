# GNIRS Prism

The prism turret selects between ordinary single-order spectroscopy and cross-dispersed spectroscopy.

**Mirror** - no cross-dispersion. A single spectral order, chosen by the order-sorting filter, along the full long
slit (99" with the short cameras, 49" with the long cameras). Used for long-slit and IFU spectroscopy, in any band
from X to M.

**SXD** (short cross dispersion) - designed for the Short Blue camera. Spreads several orders across the detector to
cover 0.85–2.5 µm in a single exposure, with a 7.0" slit.

**LXD** (long cross dispersion) - designed for the Long Blue camera. Covers 0.85–2.5 µm with a 5.1" slit.

The Long Blue camera may also be used with the SXD prism, for a longer 7.0" slit. This gives more spatial coverage along the
slit but only orders 3–5 (roughly J to K); see the **Decker** help for the decker to use.

Cross-dispersed configurations use the broad XD filter, and their default offsets along the slit are smaller to fit
the short slit (−1", +2", +2", −1").

Some combinations are not allowed, and the observation is flagged with an error if they are chosen:

- Cross-dispersion is not available in the L or M bands.
- The red cameras cannot be used with SXD or LXD.
- The Short Blue camera cannot be used with LXD.

This field can only be changed under **Advanced Customization**. A reset icon appears beside the field once it
differs from the configuration's default, to revert back to it.
