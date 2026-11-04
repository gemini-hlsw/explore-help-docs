## Requested Coordinates + Configurations + Constraints

This tile lists every combination of target coordinates, instrument configuration and observing constraints (CCC)
that has been requested for this program. It starts with the CCCs from the proposal, as decided by the TAC,
and grows as new CCCs are requested from the Unrequested Coordinates + Configurations + Constraints table below.
The number in the tile title is the number of requests.

Observations covered by an approved CCC may be set to Ready; observations whose CCC is not approved may not.
For what counts as the same CCC, and what you may change without a new approval, see the help for the
Unrequested Coordinates + Configurations + Constraints table.

### Reading the table

Each row is one request. **ID** is the request identifier, and **Status** shows where it stands
(hover over the icon to see the status name):

- 🟢 **Approved**: observations covered by this CCC may be set to Ready.
- 🟡 **Requested**: waiting for review by the Head of Science Operations.
- 🔴 **Denied**: observations using this CCC must be changed to use an approved CCC.
- ⚪ **Withdrawn**: the request was withdrawn and will not be reviewed unless it is resubmitted.

**Target**, **RA**, **Dec**, **Instrument**, **FPU**, **Configuration**, **AO**, **IQ**, **CC**, **SB** and **WV**
describe the CCC, as in the Unrequested table. **Obs** lists the observations covered by the request;
click an observation ID to open it. Inactive observations are shown struck through.

### Managing requests

Select one or more rows by clicking them (or use **All** and **None**), then use the buttons in the tile header:

**View Justification and Feedback** (book icon) shows the justification submitted with each selected request
and any feedback from the reviewer.

**Withdraw** cancels requests that have not yet been reviewed. It is available only when every selected request
has the status Requested.

**Resubmit** sends withdrawn requests for review again. It is available only when every selected request has the
status Withdrawn, and opens the Request Editor so that you can revise the justification. If the selected requests
have different justifications, the editor starts empty and the text you enter replaces all of them; select the
requests one at a time to keep their individual justifications.

Read-only Co-Investigators can view the table and the justifications and feedback, but cannot withdraw or
resubmit requests.
