# GNIRS Well Depth

The well depth sets the detector bias voltage, which determines how much charge each pixel can hold before it
saturates. It does not change the read noise or the minimum exposure time.

| Well depth | Bias   | Full well    | Non-linear above |
|------------|--------|--------------|------------------|
| Shallow    | 300 mV | 90,000 e⁻    | 5,000 ADU        |
| Deep       | 600 mV | 180,000 e⁻   | 10,000 ADU       |

**Shallow** - for near-infrared observations (X, J, H and K). This is the default for the blue cameras.

**Deep** - for thermal-infrared observations (L and M), where the sky background is high, or for very bright
targets. This is the default for the red cameras. The higher bias exacerbates defects in the detector substrate,
causing a noticeable increase in the number of noisy or "hot" pixels, so Deep should only be used when the extra
well depth is needed.

The well depth applies to the whole observation, including the acquisition, and is used by the ITC when estimating
saturation.

This field can be changed after clicking **Customize**. A reset icon appears beside the field once it differs from
the default for the camera, to revert back to it.
