## Unrequested Coordinates + Configurations + Constraints

This panel displays combinations of target coordinates, instrument configurations, and observation constraints (CCC) 
that do not match any CCC formally approved through the original proposal or through subsequent program change requests. 

### Definition of a Unique CCC

A CCC is considered unique based on the following criteria:

**Coordinates** include a positional buffer around the originally requested coordinates equal to one-half of the instrument’s field of view. 
Coordinate changes within this buffer are not treated as a new CCC.

**Configuration** includes the selected instrument, observing mode (imaging, long-slit, IFU, or MOS), and disperser. 
Changes to other parameters such as filter, central wavelength, or detector binning do not by themselves define a new CCC.

**Conditions** include the originally requested observing conditions as well as any more permissive (worse) conditions. 
Selecting worse conditions than originally requested does not create a new CCC.

For example, a user may adjust the target coordinates slightly (within the positional buffer), modify the filter, 
the central wavelength, or binning, and select worse observing conditions, all without requiring approval of a new CCC.

### Requesting Approval for a CCC

If an unrequested CCC is required, select the relevant row or rows in this table and click Request Approval. 
This action opens the Request Editor, where a justification for the proposed program changes must be provided.
Selecting Submit sends the request to the Head of Science Operations at the site of the observations. 
Once submitted, the CCC will appear in the Requested Coordinates + Configurations + Constraints table with a status of Pending until the review process is complete.
