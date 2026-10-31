# GNIRS Camera

GNIRS has four cameras, combining two pixel scales with two wavelength ranges.

| Camera     | Pixel scale | Wavelengths            | Slit length |
|------------|-------------|------------------------|------------------|
| Short Blue | 0.15"/pixel | < 2.5 µm (X, J, H, K) | 99"           |
| Short Red  | 0.15"/pixel | > 2.5 µm (L, M)    | 99"              |
| Long Blue  | 0.05"/pixel | < 2.5 µm (X, J, H, K) | 49"           |
| Long Red   | 0.05"/pixel | > 2.5 µm (L, M)    | 49"              |

**Short or long.** The short cameras are the usual choice. The long cameras give three times finer spatial
sampling, and with a narrow slit three times the spectral resolution, but a shorter slit and greater slit losses.
They are generally used with Altair adaptive optics, or when the highest spectral resolution is required.

**Blue or red.** Use a blue camera for X, J, H and K, and a red camera for L and M.

In spectroscopy, some combinations are not allowed, and the observation is flagged with an error if they are chosen:

- The red cameras cannot be used with the cross-dispersing prisms (SXD or LXD).
- The Short Blue camera cannot be used with the LXD prism; LXD is designed for the Long Blue camera, and SXD for
  the Short Blue camera.

The camera also sets several defaults:

- **Well depth** defaults to Shallow for the blue cameras and Deep for the red cameras.
- In spectroscopy, the **decker** default follows the camera's pixel scale, and so do the default
  **spatial offsets** along the slit.

In spectroscopy, this field can only be changed under **Advanced Customization**. A reset icon appears beside the
field once it differs from the configuration's default, to revert back to it. In imaging, it can be changed after
clicking **Customize**.

See the [GNIRS components page](https://www.gemini.edu/node/10530) for more details of the cameras.
