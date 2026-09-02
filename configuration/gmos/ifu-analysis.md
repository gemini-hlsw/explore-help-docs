# GMOS IFU Analysis

When an IFU is selected one may choose between two ITC analysis methods:

**Summed** - calculates the signal and noise for the sum of all elements (spaxels) inside the specified radius.
The default radius is 0.2 arcseconds which encompases a single element, and this will give identical results as "Single Element" with Offset = 0 arcseconds.

**Single Element** - calculates the signal and noise for a single element (spaxel) offset by a specified number of arcseconds from the source center.
