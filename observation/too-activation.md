# ToO Activation

Whether this observation is a [Target of Opportunity (ToO)](http://www.gemini.edu/observing/phase-i/too),
and if so, how disruptive its trigger is allowed to be to other observations already running.

| Activation | Meaning |
|---|---|
| None | Not a Target of Opportunity. Observed whenever convenient, like ordinary science. |
| Rapid | Observed as soon as possible once triggered, but does not displace an observation already running. |
| Interrupting | Observed as soon as possible once triggered, displacing an observation already running where that observation's scheduling mode permits it. |

An observation is a Target of Opportunity whenever its activation is above *None*. The choice
here cannot exceed the program's own ceiling, set in the **ToO Activation Ceiling** field of the
Program Details tile.

### Effect on scheduling

Rapid and Interrupting both require the observation's **Scheduling Mode**, in the Scheduling tile,
to be *Uninterruptible*: setting one of these activations switches the mode there automatically,
and locks the selector while the activation remains above *None*. Lowering the activation back to
*None* does not revert the mode; change it by hand if the observation no longer needs to be
uninterruptible.

Because only an Interrupting ToO can displace a running observation, and it can never displace an
Uninterruptible one, a Target of Opportunity is never interrupted by another.
