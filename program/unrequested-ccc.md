## Unrequested Coordinates + Configurations + Constraints

This tile lists the combinations of target coordinates, instrument configuration, and observing constraints (CCC)
used by active observations in this program that are not covered by any CCC approved in the original proposal
or requested since. The number in the tile title is the number of such CCCs.

Observations whose CCC appears here cannot be set to Ready until a request for that CCC has been approved.
Inactive observations and calibrations are not listed.

### Reading the table

Each row is one CCC. **Target** shows the target name, or `<multiple>` when the observations in the row use
different targets. **RA** and **Dec** are the coordinates (or a range, for a target defined as a region of sky).
**Instrument**, **FPU** and **Configuration** describe the observing mode, **AO** shows the adaptive-optics mode if any,
and **IQ**, **CC**, **SB** and **WV** are the observing constraints. **Obs** lists the observations that use the CCC;
click an observation ID to open it.

### Definition of a Unique CCC

An observation is covered by an approved CCC when all of the following hold:

**Coordinates** lie within a buffer around the approved position equal to the radius of the instrument's
science field, so the base position may be moved anywhere that was visible from the approved pointing.
For MOS the buffer is half the imaging field. A target defined as a region is covered only by an approved
region that contains it.

**Configuration** matches the approved instrument and observing mode (imaging, long slit, IFU or MOS) and the
key optical elements: the grating or disperser for spectroscopy, the IFU unit for IFU modes, the camera and prism
for GNIRS, and the resolution mode for GHOST. For imaging, the filters must be among those approved: removing a
filter is allowed, adding one is not. Other parameters, such as central wavelength, binning, read mode or
exposure times, may be changed freely. The adaptive-optics mode must match exactly.

**Constraints** are the same as, or less demanding than, the approved image quality, cloud extinction,
sky background and water vapor. Selecting worse conditions does not create a new CCC.

**Scheduling mode** is also part of the CCC, although it is not shown as a column. Approval of a more
restrictive scheduling mode covers less restrictive ones, so changing to a more restrictive mode requires approval.

For example, you may move the target slightly, drop an imaging filter, change the central wavelength or binning,
and relax the constraints without needing a new approval.

### Requesting Approval for a CCC

Select one or more rows by clicking them (or use **All** and **None**), then click **Request Approval**.
This opens the Request Editor, where you must enter a justification for the change; the same justification is
attached to every selected CCC. Click **Submit** to send the request to the Head of Science Operations at the
site of the observations. The CCC then moves to the Requested Coordinates + Configurations + Constraints table
with the status 🟡 Requested until it has been reviewed.

If a request is denied, the CCC is not offered here again. Modify the observations to use an approved CCC,
or change them to a new CCC that can be requested.

Read-only Co-Investigators can view this table but cannot request approval.
