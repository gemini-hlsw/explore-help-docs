# Binning

### x-bin $\times$ y-bin

| Instrument | x-bin    | y-bin   |
| ---------- | -------- | ------- |
| GMOS       | spectral | spatial |

The binning along each direction is chosen to be the largest that provides more than 2.5 pixel sampling across a resolution element.

In the spectral direction: 

&nbsp;&nbsp; $\lambda_{blaze} / R_{eff} / \text{dispersion} / \text{binning} > 2.5 \text{pix}$

where

&nbsp;&nbsp; $R_{eff} = R_{1" slit} / \text{min}(\text{slitwidth}, \text{FWHM})$

In the spatial direction: 

&nbsp;&nbsp; $\text{fwhm} / \text{pixscale} / \text{binning} > 2.5 \text{pix}$

Additional rules applied to the default binning:
- MOS spatial binning is capped at 2
- IFU binning is always $1 \times 1$
