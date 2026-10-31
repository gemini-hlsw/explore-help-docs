# GNIRS Decker

The decker is a mask in front of the slit that sets how much of it is used: the slit length, or the IFU field.

The decker to use follows the rest of the configuration:

| Configuration                    | Decker                       | Slit length |
|----------------------------------|------------------------------|-------------|
| Long slit, short camera          | Short camera long slit       | 99"         |
| Long slit, long camera           | Long camera long slit        | 49"         |
| Cross-dispersed, short camera    | Short camera cross dispersed | 7.0"        |
| Cross-dispersed, long camera     | Long camera cross dispersed  | 5.1"        |
| Cross-dispersed, long camera     | Short camera cross dispersed | 7.0"        |
| Low resolution IFU               | Low resolution IFU           |             |
| High resolution IFU              | High resolution IFU          |             |

The cross-dispersed deckers use a short slit so that the spectral orders do not overlap on the detector.

With the long camera, the LXD prism is the native pairing, giving full 0.85–2.5 µm coverage with the 5.1" slit.
For a longer 7.0" slit, pair the long camera with the SXD prism and the **Short camera cross dispersed** decker.
The longer slit gives more spatial coverage, for slightly extended targets or larger offsets along the slit, but
less wavelength coverage: only spectral orders 3–5 (roughly J to K). 

Changing the camera, prism or IFU updates the default decker. A decker you have chosen yourself does not change,
so revert it if you change any of these.

Choosing any other decker gives a warning naming the expected one.

The acquisition steps always use the acquisition decker automatically, and the pupil viewer is for engineering.

This field can be changed after clicking **Customize**. A reset icon appears beside the field once it differs from
the configuration's default, to revert back to it.
