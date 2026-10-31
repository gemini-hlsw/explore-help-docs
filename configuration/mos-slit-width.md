# MOS Slit Width

The slit width to assume for a MOS mask, chosen from the instrument's standard list of slit widths. 
A reset icon appears beside the field once it differs from the configuration's default, to revert back to it.

Once the proposal has been accepted and a mask is bound in **Mask ID**, the physical mask defines
the actual slit width, so this field switches to showing that value read-only rather than letting
it be entered by hand. Before a mask is bound — including before the proposal has been accepted,
when there is nothing yet to bind — the width is set here directly, as the best estimate for
planning the observation's time and sensitivity.
