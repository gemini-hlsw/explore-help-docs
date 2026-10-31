# Groups

A group collects observations, or other groups, that the Scheduler should treat together. There
are two kinds, chosen with the **Type** selector when the group is created:

| Type | Behavior |
|---|---|
| AND (Scheduling) | Every observation in the group is scheduled, subject to the timing rules set here. |
| OR (Choose *n*) | Only *n* of the observations in the group are scheduled; once one of them has started, the others are no longer considered. |

### AND groups

* **Ordered** — the observations are scheduled in the order they are listed, each only after the
  previous one has completed. Left unchecked, the Scheduler may run them in any order.
* **Same Night** — every observation in the group must be scheduled on the same night.
* **Minimum delay** / **Maximum delay** — how long after one observation completes the next may
  start. A maximum delay cannot be set together with Same Night; enabling one clears the other.
  The minimum must not exceed the maximum.

The Scheduler always respects each observation's own absolute timing constraints in addition to these relative group-level rules.

### OR groups

**Observe *n* of *m* observations/subgroups** sets how many of the group's members are needed.
Once that many have been selected and started, the rest are dropped from future scheduling.

### Planned Time

Shown once the group contains observations with a time estimate. When every path through the
group takes the same time, a single **Planned Time** is shown; otherwise a **Maximum** and a
**Minimum Planned Time** are both shown, covering the range the group could take depending on
which observations run. The figure is dimmed with a tooltip while a recalculation is in progress.

### System groups

Groups the system creates automatically, such as the Calibrations group, have no Type selector
and cannot be edited here.
