# UQSH CMB-Stacking Analysis

**Author:** Ukshin Q. Rexhepi  
**Institution:** Independent Researcher, Tübingen, Germany  
**ORCID:** https://orcid.org/0009-0003-4145-5431  
**Date:** April 2026  

---

## Overview

This repository contains a reconstruction of a CMB stacking analysis 
testing a prediction of the Universal Quantum Foam Hypothesis (UQSH).

The analysis investigates whether cosmic voids in the local universe 
(z < 0.03) exhibit a measurable temperature deviation in the Cosmic 
Microwave Background (CMB).

Within the UQSH framework, voids are expected to appear slightly warmer 
due to reduced local field tension. This contrasts with the standard 
cosmological model (ISW effect), which predicts voids to appear colder.

---

## Main Result

| Measurement | Temperature Difference | Significance |
|-------------|----------------------|--------------|
| This analysis (N=83 voids) | +2.9 µK | 0.6 sigma |
| Hansen et al. (2025) | +41 µK | 6.5 sigma |
| Standard model (ISW) | negative | expected |

The sign of the measured effect is **consistent with the UQSH prediction** 
and with Hansen et al. (2025).

The statistical significance is limited by the small sample size of the 
2MRS catalog at z < 0.03.

---

## Achromatic Test

The temperature difference was evaluated across:

- Planck SMICA
- Planck SEVEM 143 GHz
- Planck SEVEM 217 GHz

The signal is consistent across frequencies, indicating:

- no frequency-dependent interaction  
- compatibility with a scaling process rather than scattering  

---

## Method

- **Void finder:** Sparkling (Ruiz et al. 2015, 2019)  
- **Galaxy catalog:** 2MRS (Huchra et al. 2012)  
- **CMB map:** Planck SMICA 2048 (ESA, 2018)  
- **Stacking:** concentric rings normalized to void radius  
- **Redshift range:** z < 0.03  
- **Galactic mask:** |b| > 15 degrees  
- **Quadrupole/dipole:** removed  

---

## Reproducibility

This repository is based on a **reconstruction approach**.

The original pipeline included:

- dynamic loading of the 2MRS catalog via Vizier  
- compilation and execution of the Sparkling void finder  
- stochastic procedures (random rotations, density classification)  

These steps are **not re-executed** here.

Instead, the analysis is reconstructed from preserved data products:

- `sparkling_voids.dat` (void catalog, 83 voids)  
- `results_final.txt`  
- `ergebnisse_achromatisch.txt`  
- final plots  

---

## Notebook

The repository contains a single reconstruction notebook:
notebook/UQSH_CMB_Stacking.ipynb

This notebook:

- documents the analysis  
- regenerates stable figures  
- displays original pipeline outputs for sensitive results  

UQSH-CMB-Analysis/
├── notebook/
│ └── UQSH_CMB_Stacking.ipynb
│
├── UQSH_CMB_v1/
│ ├── sparkling_voids.dat
│ ├── results_final.txt
│ ├── plot_01_cmb.png
│ ├── plot_02_2mrs.png
│ ├── plot_03_stacking_final.png
│ ├── plot_05_sparkling_voids.png
│ └── COM_CMB_IQU-smica_2048_R3.00_full.fits
│
├── UQSH_CMB_v2/
│ ├── COM_CMB_IQU-143-fgsub-sevem_2048_R3.00_full.fits
│ ├── COM_CMB_IQU-217-fgsub-sevem_2048_R3.00_full.fits
│ └── results/
│ ├── plot_achromatisch.png
│ └── ergebnisse_achromatisch.txt
│
└── README.md

---


---

## Physical Interpretation

Within the UQSH framework:

- cosmic voids correspond to regions of reduced field organization  
- reduced field tension allows slightly higher dynamical activity  
- this manifests as a small positive temperature excess  

The effect is:

- local (z < 0.03)  
- weak but systematic  
- achromatic  

---

## References

- Hansen et al. (2025), arXiv:2506.08832  
- Dominguez Feldman et al. (2025), arXiv:2506.08833  
- Planck Collaboration (2018)  
- Huchra et al. (2012)  
- Ruiz et al. (2015)  

---

## MIT License

Copyright (c) 2026 Ukshin Q. Rexhepi

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
