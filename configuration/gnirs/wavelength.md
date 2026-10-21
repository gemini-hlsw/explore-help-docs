# GNIRS Central Wavelengths

Unlike other instruments, a GNIRS spectroscopy configuration can request more than one central
wavelength: each row here becomes its own entry in the sequence, with its own exposure settings,
ITC calculation and calibrations. At least one row is required.

Each row has a **λ Center**, an exposure mode (**Signal/Noise** or **Exp. Time**), a **Number of
Exp.**, **Coadds**, and — set together with the Signal/Noise mode — the wavelength the signal-to-
noise is measured at (**λ for S/N**).

Drag a row by its handle to reorder it; the order here is the order the sequence uses. Use the ✚
button to add a row, which starts as a copy of the last one, and the trash icon to remove one.
For an unobserved telluric standard, the trash icon is replaced by a reset-to-derived button,
since a telluric's wavelengths are expected to follow its science observation rather than be
removed by hand.

If this configuration started from the proposal's requirements, the panel header shows an icon to
revert the whole list back to its original, requirement-derived set.
