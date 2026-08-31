# GMOS Central Wavelength




Note that the central wavelength may be adjusted to maximize wavelength coverage.
For example, with B480 + GG455 the range is 460-920 nm and the simultaneous coverage is 390 nm, so if the input wavelength is closer than 390/2=195 nm from an edge the central wavelength will be at 195 nm from the edge:
```
Low λc limit:  460 + 195 = 655 nm
High λc limit: 920 - 195 = 725 nm

Input λ = 600  -> λc = 655 nm
Input λ = 700  -> λc = 700 nm
Input λ = 800  -> λc = 725 nm
```
