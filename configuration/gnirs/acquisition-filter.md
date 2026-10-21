# GNIRS Acquisition Filter

The filter used for the acquisition image. Left unset, it is chosen automatically to match the
science wavelength: the order filter whose range covers it, or for science above 2.5 µm (where
science is acquired on the blue camera) a fixed thermal-IR filter instead. Override it here if
your target needs a different one — for example the H2 narrow-band filter for a very bright
target, to avoid saturation.

A reset icon appears beside the field once it differs from the automatic choice, to revert back
to it.
