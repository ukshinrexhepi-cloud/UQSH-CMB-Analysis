# UQSH CMB-Stacking Analysis

**Author:** Ukshin Q. Rexhepi  
**Institution:** Independent Researcher, Tübingen, Germany  
**ORCID:** [0009-0003-4145-5431](https://orcid.org/0009-0003-4145-5431)  
**Date:** April 2026

---

## Overview

This repository contains the complete code for an empirical analysis of 
the Cosmic Microwave Background (CMB) within the framework of the 
Universal Quantum Foam Hypothesis (UQSH).

The analysis tests the UQSH prediction that cosmic voids in the local 
universe (z < 0.03) should exhibit a slightly elevated effective CMB 
temperature, as a consequence of the reduced local field tension state 
of the Qu-foam. This contrasts with the standard model expectation 
(ISW effect), which predicts voids to appear colder than average.

---

## Main Result

| Measurement | Temperature Difference | Significance |
|-------------|----------------------|--------------|
| This analysis (N=83 voids) | +2.9 µK | 0.6 sigma |
| Hansen et al. 2025 | +41 µK | 6.5 sigma |
| Standard model (ISW) | negative | expected |

The sign of the measured effect is **consistent with the UQSH prediction** 
and with Hansen et al. (2025, arXiv:2506.08832). The lower significance 
is attributed to the smaller sample size compared to Hansen et al.

---

## Method

- **Void finder:** Sparkling (Ruiz et al. 2015, 2019)
- **Galaxy catalog:** 2MRS (Huchra et al. 2012, J/ApJS/199/26)
- **CMB map:** Planck SMICA 2048 (ESA, 2018)
- **Stacking:** Concentric rings normalized to void radius
- **Redshift range:** z < 0.03
- **Galactic mask:** |b| > 15 degrees
- **Quadrupole/dipole:** removed (following Hansen et al. 2025)

---

## Reproduction

### Requirements

- Google Colab (free tier sufficient)
- Google Drive with at least 3 GB free storage
- Planck SMICA map (download required, see below)

### Step 1: Download the Planck CMB Map

- https://irsa.ipac.caltech.edu/data/Planck/release_3/all-sky-maps/maps/component-maps/cmb/COM_CMB_IQU-smica_2048_R3.00_full.fits

### Step 2: Open the Notebook

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ukshinrexhepi-cloud/UQSH-CMB-Analysis/blob/main/UQSH_CMB_Stacking.ipynb)

### Step 3: Run All 6 Blocks in Order

| Block | Content | Duration |
|-------|---------|----------|
| 1 | Installation and imports | 2 min |
| 2 | Load Planck CMB map | 3 min |
| 3 | Load 2MRS galaxy catalog | 1 min |
| 4 | Compile Sparkling and find voids | 5 min |
| 5 | CMB stacking analysis | 3 min |
| 6 | Save plots and results | 1 min |

---

## Repository Structure

- UQSH-CMB-Analysis/
├── UQSH_CMB_Stacking.ipynb     # Main notebook
├── README.md                    # This file
├── results/
│   ├── ergebnisse_final.txt    # Numerical results
│   └── sparkling_voids.dat     # Void catalog (83 voids)
└── plots/
├── plot_01_cmb.png         # Planck CMB map
├── plot_02_2mrs.png        # 2MRS redshift distribution
├── plot_05_sparkling_voids.png  # Void positions on sky
└── plot_03_stacking_final.png   # Main result

---

## Physical Interpretation

Within the UQSH framework, the observed temperature excess in void 
directions is interpreted as a local field tension effect. Voids 
represent regions of minimal field organization in the Qu-foam. 
The reduced local field tension allows for slightly higher free 
dynamical activity, which manifests as a marginally elevated effective 
temperature of the propagating boundary dynamics arriving from those 
directions.

This effect is predicted to be detectable only at low redshifts 
(z < 0.03), where the path through the void constitutes a significant 
fraction of the total propagation distance. At larger redshifts, the 
effect is averaged out over the full path, consistent with the observed 
CMB homogeneity at cosmological scales.

The achromatic nature of the temperature difference, confirmed by 
Dominguez Feldman et al. (2025) for filaments, is a direct structural 
prediction of the UQSH framework: the scaling factor sigma(gamma) acts 
uniformly on all frequency components of a boundary dynamics, producing 
no frequency-selective interaction.

---

## References

- Rexhepi, U.Q. (2026). *The Cosmic Microwave Background within the UQSH*. Figshare.
- Hansen, F.K. et al. (2025). *Evidence for a sign change of the ISW effect in the very recent Universe*. arXiv:2506.08832
- Dominguez Feldman et al. (2025). *Cosmic filaments confirm unexplained CMB temperature decrements*. arXiv:2506.08833
- Huchra, J.P. et al. (2012). *The 2MASS Redshift Survey*. ApJS 199, 26
- Planck Collaboration (2018). *Planck 2018 results VI*. A&A 641, A6
- Ruiz, A.N. et al. (2015). *Sparkling: a spherical void finder*. ApJ 801, 139

---

## License

MIT License. Free use with attribution.

---

## Related Preprints

- [Ontological Framework (UQSH)](https://figshare.com)
- [Spectral Shift, Time Dilation and Intensity Decrease (UQSH)](https://doi.org/10.6084/m9.figshare.31564024)
- [Light in Light, Redshift and the CMB in the UQSH](https://doi.org/10.6084/m9.figshare.31369846)
- [The Fractal Universe (UQSH)](https://doi.org/10.6084/m9.figshare.31813897)
