# Integration Time Calculator Plots

The has two plots which may be selected using the buttons in the bottom right corner:

1. S/N

2. Signal

For observations with more than one target use the pull-down menu in the ITC panel title bar to select which target you would like to see plots of.

---

### Image Size and Aperture

The derived image size (FWHM of the assumed Gaussian PSF) includes contributions from seeing, telescope diffraction, the performance of the tip-tilt secondary and many other components. See the [image quality](../../../constraints/main/iq.md) in the observing condition constraints for more details of the wavelength dependence and frequency of occurrence. For the adaptive optics case both the FWHM of the AO-corrected core and the FWHM of the uncorrected halo are given, as is the Strehl ratio.

The "optimum aperture" size is described on the analysis methods page.

For most uniform surface brightness (USB) calculations, the (assumed circular) software aperture corresponds to an area of 1 arcsec^2 when the "optimum aperture" analysis option is selected. (A different value can be specified by the user and the point source size is also reported for reference). However in the case of the GMOS IFU, the "optimum aperture" option corresponds to a single IFU spatial element (not 1 arcsec^2) and the spectra from that IFU fiber (nominally 5 detector rows) are summed. No optimal extraction or deconvolution is performed at this time.


In the cross-dispersed mode with GNIRS, the source signal and sqrt(background) are color-coded for each order with dark and light shades of the same color. Only the final S/N plot (i.e. not the single-exposure chart) is shown.

To view (or save) the spectra as ASCII files with tab-separated columns, click (or shift+click) on the link(s) under each plot. The wavelength units are nm; the ordinate has the same units as the graphics plot. 


Signal to noise calculations
See the calculation and analysis methods for more details on how the S/N for the whole observation is derived.


Error messages - most are self explanatory; others:
Can't find sourceGeom - usually occurs when trying to use the ITC from Netscape 6.x which doesn't work with forms.
Please use a model line width > 1 nm to avoid undersampling of the line profile when convolved with the transmission response - the ITC currently samples the sky transmission spectrum, background and many other optical elements at 0.25-0.5nm resolution. Hence any model emission line that is narrower than 1nm may not be correctly propagated through the calculator. 
 
### Calculation methods

There are two modes available:

1. Calculate the total signal-to-noise ratio (S/N) for an observation with the specified exposure time, number of exposures and sky subtraction method

2. Calculate the total integration time to achieve the requested S/N for an observation with the specified exposure time and sky subtraction method

As the S/N can vary markedly with wavelength, particular in the infrared, only the former mode is available for spectroscopic calculations.

The Integration Time Calculator reports the total signal and noise for a single exposure and the signal-to-noise ratio (S/N) for a single exposure and for the whole observation. In general, the theoretical S/N (reported by the ITC as the "intermediate S/N") for a single exposure is not achievable because it is necessary to perform sky or background subtraction. In practice there are many ways to achieve this subtraction depending on the frequency of sky observations, the spatial extent of the object (e.g. it may be necessary to observe separate sky frames in a crowded field or for an extended object) and the personal preference of the observer.

The ITC uses an approximation that each on-source exposure measures both signal and noise and that the process of background subtraction adds another contribution of noise. (This is a generally applicable case; it can be shown that this approximation is within 0.5 to sqrt(3) of other approaches to background subtraction). In this case the final S/N is:

final S/N = $\frac{\sqrt{number of on-source exposures} \times signal}{\sqrt{signal + 2 \times (sourceless noise)^2}}$

where "aperture ratio" is (1 + source aperture area / sky aperture area). For some instruments the aperture ratio may be defined by the user in the ITC; in others (e.g. NIRI) it is fixed equal to unity at present. The 'sourceless noise' is defined as the (quadratic) combination of background, readout and dark current noise:

sourceless noise = $\sqrt{var(background) + var(readout) + var(dark)}$

where var(background) is the square of the background noise (i.e. the background flux) etc. and the number of on-source exposures is:

number of on-source exposures = number of exposures $\times$ fraction with source

Several examples should clarify the behaviour of this algorithm. In each case we assume that the source is faint so that the observation is (sky + telescope) background noise limited and set the aperture ratio to 2.

1. Let the total number of exposures be 1. The ITC reports a final S/N that is worse than that derived intrinsically for the single exposure because it assumes background subtraction mst be performed.

2. Let the total number of exposures be 4 all of which are on-source (e.g. we have offset the telescope but kept the target within the detector or slit field of view). The on-source integration time is 4t. The final S/N is sqrt(2) better than an observation with 2 exposures (integration time 2t) as we have doubled the on-source integration time.

3. Let the total number of exposures be 4 but only 2 of which are on-source (e.g. we have offset the telescope to blank sky because the source is large or are chopping and nodding off-chip). The on-source integration time is 2t. The final S/N is sqrt(2) worse than case (2) and the same as an observation with 2 on-source exposures.

### Analysis methods

In both imaging and spectroscopy modes the signal and total noise is calculated within a software aperture optimised to yield the best S/N ratio or within an aperture specified by the user. The 'optimum' aperture differs slightly for bright and faint sources (i.e. it depends on the dominant source of noise) but an effective compromise over a wide range of source brightness is 1.18 * FWHM for imaging a point source (see the notes associated with the IRAF routine noao.astutil.ccdtime for further information). This aperture contains 61% of the total signal for the assumed Gaussian PSF. (See the more details of the default aperture used in the AO case).

In the case of a uniform surface brightness (USB) source the 'optimum' aperture simply defaults to an area of one sq arcsec. Depending on the dominant source of noise, larger apertures will typically give higher S/N in the USB case.

For spectroscopy, the equivalent length integrated along the slit that yields the best S/N ratio would be 1.4 * FWHM for a Gaussian PSF. For computational simplicity, the ITC rounds this length to an integer number of pixels.

When calculating the area enclosed by the software aperture in the imaging case, the minimum is 9 pixels.

The ITC results page reports the aperture used by the software, the fraction of the source flux it contains and the source + background signal in the peak pixel.

### Adaptive Optics in the ITC

The ability of the AO system to correct the wavefront depends on the brightness and off-axis angle of the wavefront reference source (the AO "guide star"). The Strehl ratio of the AO-corrected core is approximated in the ITC by:

$S = S_{fit} \times S_{noise} \times S_{aniso}$

$S_{fit} = e^{ -0.04 \times ( \frac{D}{r_0(\lambda)})^{5/3} }$

$S_{noise} = e^{ (\frac{-1650}{\lambda})^2 (\frac{ R_{GS} }{14} )^{16} }$

$S_{aniso} = e^{ (\frac{-1650}{\lambda})^2 (\frac{\theta_{GS}}{12.5})^2 }$

where $S_{fit}$ is the Strehl due to the system fitting error (i.e. limited number of actuators), $S_{noise}$ is the Strehl loss due to the limited number of photons from the guide star and $S_{aniso}$ is the Strehl loss due to anisoplantism. $R_{GS}$ is the R-band guide star magnitude and $\theta_{GS}$ is the off-axis angle in arcsec.

The total signal from a point source is the sum of the AO-corrected core and the uncorrected (seeing-limited) halo. For moderate or high Strehl ratios the core dominates, for poor correction (low Strehl) the halo dominates. As in the non-AO case, the ITC defaults to an "optimum" aperture which gives a reasonable approximation of the best S/N ratio; we have taken this to be 1.18 * FWHMAO, where FWHMAO is the width of the corrected core: 

### Telescope Properties

#### Mirror coating

The Gemini coating chamber is capable of depositing either alumini(u)m or silver. Currently the primary, secondary and tertiary (science fold) mirrors on both telescopes are silver coated. This [graph] shows the reflectivity of Al and Ag.

#### Instrument port

Gemini facility instruments may be mounted either on a side-looking or the up-looking ports of the instrument support structure (ISS). When mounted on a side port they are fed by reflection off the science fold mirror which incurs an additional small loss in transmission and an associated increase in emissivity. For signal-to-noise calculations it should be assumed that the instrument is side-looking. The default location for mid-IR instruments (e.g. T-ReCS, Michelle) is the up-looking port and is the side port for other instruments. 

#### Wavefront sensor

Use of a peripheral wavefront sensor (PWFS) or an on-instrument wavefront sensor (OIWFS) is required to provide tip-tilt error signals for the image motion compensation by the secondary mirror. Not all instruments have an OIWFS; see the specific instrument pages for details. When present, the OIWFS allows selection of a WFS star closer to the science field and therefore usually provides better image motion compensation and smaller images (see the image quality section of the observing condition constraints page for more details).
