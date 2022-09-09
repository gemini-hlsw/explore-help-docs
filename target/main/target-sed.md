# Spectral Energy Distribution

The source spectrum is selected from the available libraries of stellar and non-stellar spectra, model emission line + continuum, black body, power law, and user-defined spectra. Different options are available depending on the instrument in question. The spectrum may be redshifted by an arbitrary amount. If the selected (redshifted) spectrum does not completely cover the observing wavelength range, as defined by the colour filter or dispersive element, either an error is reported by the ITC or the spectrum is padded with leading or trailing zeros.

For spectroscopic calculations, the source spectrum is smoothed to the resolution of the spectrograph as given by the dispersing element with an entrance aperture defined by the slit width, or source extent if narrower (some exceptions are noted for specific instruments). Note that the stellar and non-stellar libraries may have an intrinsic resolution less than that of the instrument or a coarser sampling. In all cases they are re-sampled to the appropriate dispersion within the ITC.

The sky transmission and sky background spectra employed currently have a resolution of ~1nm and sampling of ~0.5nm. Hence at higher instrument spectral resolutions, the sky lines will not be treated correctly.

(a) Non-stellar library

Rest-frame optical and near-IR spectra:

- Mars is a composite spectrum from [Norwood et al, 2016, PASP, 128, 25004](https://ui.adsabs.harvard.edu/abs/2016PASP..128b5004N) using the visible to near-IR albedo spectrum from [McCord, T. B., Elias, J. H., & Westphal, J. A. 1971, Icar, 14, 245](https://ui.adsabs.harvard.edu/abs/1971Icar...14..245M), and the 2.5 - 5 micron ISO spectrum from [Lellouch, E., Encrenaz, T., de Graauw, T., et al. 2000, P&SS, 48, 1393](https://ui.adsabs.harvard.edu/abs/2000P%26SS...48.1393L).

- Jupiter and Saturn are composite spectra from [Norwood et al, 2016, PASP, 128, 25004](https://ui.adsabs.harvard.edu/abs/2016PASP..128b5004N) using the visible to near-IR albedo spectra from [Clark, R. N., & McCord, T. B. 1979, Icar, 40, 180](https://ui.adsabs.harvard.edu/abs/1979Icar...40..180C), the visible to 1 micron geometric albedo spectrum from [Karkoschka, E. 1994, Icar, 111, 174](https://ui.adsabs.harvard.edu/abs/1994Icar..111..174K), and the 2.5 - 5 micron ISO spectrum from [Encrenaz, T., Lellouch, E., Feuchtgruber, H., et al. 1997, in Proc. First ISO Workshop on Analytical Spectroscopy, ESA-SP, 419, 125](https://ui.adsabs.harvard.edu/abs/1997ESASP.419..125E).

- Uranus and Neptune are composite spectra from [Norwood et al, 2016, PASP, 128, 25004](https://ui.adsabs.harvard.edu/abs/2016PASP..128b5004N) using the visible to near-IR albedo spectra from [Fink, U., & Larson, H. P. 1979, ApJ, 233, 1021](https://ui.adsabs.harvard.edu/abs/1979ApJ...233.1021F), the visible to 1 micron geometric albedo spectra from [Karkoschka, E. 1994, Icar, 111, 174](https://ui.adsabs.harvard.edu/abs/1994Icar..111..174K/), the 2.5 - 5 micron Akari albedo spectrum of Neptune (scaled for Uranus) from [Burgdorf, M. J., Drossart, P., Encrenaz, T., Fletcher, L. N., & Orton, G. 2008, BAAS, 40, 489](https://ui.adsabs.harvard.edu/abs/2008DPS....40.5009B/), and the 2.6-4um ISO spectra from [Encrenaz, T., Lellouch, E., Feuchtgruber, H., et al. 1997, in Proc. First ISO Workshop on Analytical Spectroscopy, ESA-SP, 419, 125](https://ui.adsabs.harvard.edu/abs/1997ESASP.419..125E).

- Elliptical galaxy is a template spectrum (class T=-5, -4) covering the wavelength range 22 - 10000 nm and taken from the Pegase Atlas of Galaxies by [Fioc & Rocca-Volmerange, 1997, A&A, 326, 950F](https://ui.adsabs.harvard.edu/abs/1997A%26A...326..950F). The spectrum has a sampling of 1nm at wavelengths shortwards of 878nm and 20nm longwards.

- Spiral (Sc) galaxy is a template spectrum (type Sc, class T=5) covering the wavelength range 22 - 10000 nm taken from the Pegase Atlas of Galaxies by [Fioc & Rocca-Volmerange, 1997, A&A, 326, 950F](https://ui.adsabs.harvard.edu/abs/1997A%26A...326..950F). The spectrum has a sampling of 1nm at wavelengths shortwards of 878nm and 20nm longwards.

- QSO covers the (rest) wavelength range 80 - 855 nm with a spectral resolution ~1800 and a sampling of 0.1nm and is taken from [Vanden Berk et al. 2001, AJ, 122, 549](https://ui.adsabs.harvard.edu/abs/2001AJ....122..549V).

- QSO2 covers the (rest) wavelength range 276 - 3520 nm with a sampling of 0.1nm and is taken from [Glikman et al. 2006, ApJ, 640, 579](https://ui.adsabs.harvard.edu/abs/2006ApJ...640..579G).

- HII region (Orion) covers the wavelength range 100 - 1100 nm with a sampling of 0.05nm and was taken from the HST STIS exposure time calculator.

- Planetary nebula (NGC7009) covers the wavelength range 100 - 1100 nm with a sampling of 0.05nm and was taken from the HST STIS exposure time calculator.

- Planetary nebula 2 (IC5117) covers the wavelength range 480 - 2500 nm with a sampling of 0.05nm and is taken from correspondence with Rick Rudy, based on [Rudy et al. 2001, AJ, 121, 362](https://ui.adsabs.harvard.edu/abs/2001AJ....121..362R%2F).

(b) Mid-IR spectra:

A range of astronomical objects, including:

- Stellar spectra - types F-M, Wolf Rayets, carbon stars

- Other galactic objects - Galactic Centre, planetary nebula, pre-main-sequence star, young stellar object, reflection nebula, dusty HII region...

- Galaxy spectra - starburst nucleus, Seyfert II nucleus

(c) Stellar Libraries

The Pickles stellar library ([1998; PASP, 110, 863](https://ui.adsabs.harvard.edu/abs/1998PASP..110..863P)) covers optical and near-IR wavelengths out to 2.5um across a broad range of spectral types (O5 to M9) and luminosity classes (I, III and V). We have extended these spectra out to 6um, arbitrarily adopting the slope of the K0III star for all spectral types. More accurate spectrophotometry will be inserted in the ITC library as it becomes available.

Model spectra for cool stars and brown dwarfs are provided from effective temperatures of 2800 K to 400 K. For temperatures down to 1200 K, the spectra are the version of [BT-Settl models](https://phoenix.ens-lyon.fr/Grids/BT-Settl/CIFIST2011_2015/) ([Allard et al. 2012](https://ui.adsabs.harvard.edu/abs/2012RSPTA.370.2765A/)) that were used in the [BHAC 2015](https://ui.adsabs.harvard.edu/abs/2015A%26A...577A..42B) evolutionary models. Below 1200 K, the spectra are models from [Morley et al. (2012)](https://ui.adsabs.harvard.edu/abs/2012ApJ...756..172M) that have thin clouds (fsed=5). All models correspond to solar metallicity, and surface gravity is log(g) = 5.5 dex (cgs) down to 1800 K, 5.0 dex (cgs) down to 800 K, and 4.5 dex (cgs) down to 400 K.

(d) Single Emission Line and Continuum
This generates a Gaussian emission line on top of a flat (per wavelength interval) continuum. The specified line flux and continuum flux density override the brightness normalization defined as part of the spatial profile. If using a uniform surface brightness spatial profile the fluxes are per square arcsecond.

(e) User-Defined Spectrum
User-defined source spectra can be used instead of the existing template and model SEDs. Note the following restrictions on file format:

- Two columns separated by spaces:
  1. Wavelength in nm
  2. Flux density in arbitrary wavelength units, e.g. per nm or per um, but not per Hz

- Files may have any number of comment lines, each starting with the # character, and any number of blank lines.
Wavelength interval need not be uniform.

- The wavelength range must extend to include both the full instrument coverage and the requested normalization filter (or wavelength). For example, a user-defined spectrum for T-ReCS must extend to below 2000nm if the source brightness is defined in the K-band.

- The file size must be less than 1MB.
