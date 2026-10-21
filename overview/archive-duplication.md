# Archive Duplication Search

Checks each observation's target and configuration against the
[Gemini Observatory Archive](https://archive.gemini.edu) (GOA), to flag science that may already
have been observed. Calibration observations are not checked.

The **Matches** column shows how many archived files were found for each observation:

| Icon | Meaning |
|---|---|
| spinner | Loading the stored result, or a new Search is running. |
| ? | Not checked yet. |
| a number | The number of matches found, or that number with a `+` if the search hit its limit and more may exist. |
| ⏱ next to a number | The observation has changed since this search ran; re-check it to bring the count up to date. |
| ⚠ | The last Search failed, or the result could not be loaded. The count shown, if any, may be out of date. |
| n/a | The archive cannot be searched for this observation. |

Click the ▸ next to an observation to expand it and see the individual Archive Matches it found,
each with its own row of the same columns: target, position, instrument, disperser, wavelength,
filter, observation date, release date, exposure, data label, angular distance from the
observation's target, archive program and observation reference, and QA state. Several of these
columns are hidden by default; use the column picker in the title to show them.

### Running a search

The ↻ button at the right of an observation's row re-checks that one observation.
**Run check** in the title runs the search for every observation that has never been checked,
whose last attempt failed, or that has changed since it was last checked — up to four at a time.
The button shows how many observations that is, and is disabled once every observation is up to
date.

A note below the title says how many observations could not be checked at all, with their labels
in a tooltip.

### When searches cannot run

The Search controls are disabled, with the reason given in their tooltip, when you do not have
permission to edit the program, or once the proposal has been submitted — submission freezes the
Archive Duplication Search along with the rest of the proposal.
