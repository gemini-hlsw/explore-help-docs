# Scheduling Mode

The scheduling mode tells the Scheduler what it is allowed to do *to* this observation once it
has been planned: whether the sequence may be split across several visits, and whether it may be
interrupted while it is executing.

| Mode            | Split across visits | Can be interrupted |
|-----------------|:-------------------:|:------------------:|
| Unconstrained   | Yes                 | Yes                |
| No Splitting    | No                  | Yes                |
| Uninterruptible | No                  | No                 |

**Unconstrained** (default): the Scheduler may execute the sequence in several visits, on the
same or different nights, and an ongoing visit may be interrupted (for example, by an
interrupting Target of Opportunity). Work completed before an interruption is kept and the
remainder can be observed later. Use this unless your science requires otherwise.

**No Splitting**: the Scheduler will only plan the sequence as a single, complete visit. The
visit may still be interrupted, but in that case the work is abandoned and the sequence is
restarted from the beginning at a later time rather than continued in a second visit. Choose
this when the data are only useful if obtained together, e.g. for a time series or for
observations that must share the same conditions.

**Uninterruptible**: the sequence must run from start to finish in one visit, and nothing can
interrupt it once it has started. This is the most restrictive mode and reduces scheduling
flexibility, so use it only when it is truly required.

### Targets of Opportunity

Observations with a ToO activation of **Rapid** or **Interrupting** are always
**Uninterruptible**. Setting one of these activations automatically switches the scheduling mode
to Uninterruptible, and the mode selector is locked while the ToO activation remains. Lowering the
activation back to **None** leaves the mode as Uninterruptible; change it manually if desired.

Because only an Interrupting ToO can interrupt other observations, and it can never interrupt an
Uninterruptible one, a Target of Opportunity is never interrupted by another.
