# Region

A Target of Opportunity has no coordinates when the proposal is written.
Instead one declares the **region** of sky the trigger is expected to fall in.

The region is the area common to two arcs: one in right ascension and one in declination. 
Each is set independently with the **RA Arc** and **Dec Arc** selectors.

| Arc | Covers |
|---|---|
| Full | The whole range of that coordinate. |
| Partial | A range between a start and an end value, which appear as two fields below the selector. Both ends are included in the arc. |

A new Target of Opportunity starts with both arcs set to *Full*, that is, the whole sky. Narrow
the region as far as your science case allows: a smaller region gives a better idea of where the 
trigger will be and improves the Observatory's ability to efficiently fill the queue.

### Partial arcs

Choosing *Partial* fills the fields with a starting range you can then edit: 00:00:00 to 12:00:00
in RA, and -90° to +90° in Dec. RA arcs run clockwise, in the direction of increasing right
ascension, so an arc whose end is smaller than its start is the one that passes through 0h. For
example, a start of 23:00:00 and an end of 01:00:00 covers the two hours around 0h, not the other
twenty-two.

Switching an arc back to *Full* or *Empty* discards its start and end values.

### Asterisms

A Target of Opportunity may be the only target in its observation. 
The option to add a ToO target is only available while the observation has no targets.
