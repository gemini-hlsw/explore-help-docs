# Scheduling Windows

Timing windows restrict *when* this observation may be scheduled, in UTC. With none defined the
observation may be scheduled at any time; each window narrows or excludes a range.

Click **Window** to add one, starting now and running forever; click a row to select it and edit
it below, and the trash icon to delete it. A window with an error, such as a start after its end,
is marked with a warning icon.

### Editing a window

* **Include** / **Exclude** — whether the observation may only be scheduled during this window,
  or may not be scheduled during it.
* **from** — when the window starts.
* **Forever** — the window has no end.
* **Through** — the window ends at a specific date and time, which must be after the start.
* **For** — the window lasts a given duration from its start.
  * A window ending this way can **Repeat with a period of** another duration, starting from the
    end of the first occurrence. A repeating window can recur **Forever**, or stop after a chosen
    number of **times**.

Add as many windows as you need; each one is independent, and an **Exclude** window can be used
to carve a gap out of a broader **Include** window.

### Read-only windows

If every observation currently selected is completed, the windows are shown read-only. If only
some are completed, the tile warns that only the uncompleted ones will be changed.
