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
| Hansen et al. 2025 | +41 µK | 6.5 sigma |
| Standard model (ISW) | negative | expected |

The sign of the measured effect is **consistent with the UQSH prediction** 
and with Hansen et al. (2025).

The lower statistical significance is attributed to the smaller sample size.

---

## Achromatic Test

The temperature difference is evaluated across:

- Planck SMICA
- Planck SEVEM 143 GHz
- Planck SEVEM 217 GHz

The effect is consistent across frequencies, indicating:

- no frequency-dependent interaction  
- compatibility with a scaling process rather than scattering  

---

## Method

- **Void finder:** Sparkling (Ruiz et al. 2015, 2019)
- **Galaxy catalog:** 2MRS (Huchra et al. 2012)
- **CMB map:** Planck SMICA 2048 (ESA, 2018)
- **Stacking:** Concentric rings normalized to void radius
- **Redshift range:** z < 0.03
- **Galactic mask:** |b| > 15 degrees
- **Quadrupole/dipole:** removed

---

## Reproducibility

The original analysis pipeline included:

- dynamic loading of the 2MRS catalog via Vizier
- compilation and execution of the Sparkling void finder
- processing of large Planck FITS maps (~2 GB)

These steps are **not re-executed** in this repository.

Instead, the analysis is reconstructed from preserved data products:

- `sparkling_voids.dat` (void catalog, 83 voids)
- result files
- generated plots

This ensures deterministic and reproducible results without external dependencies.

---

## How to Use

### Option 1 (recommended)

Open the notebook in Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ukshinrexhepi-cloud/UQSH-CMB-Analysis/blob/main/UQSH_CMB_Stacking.ipynb)

Then:

1. Mount Google Drive  
2. Ensure the data folders exist (`UQSH_CMB`, `UQSH_CMB_v2`)  
3. Run all cells  

---

## Repository Structure
UQSH-CMB-Analysis/
├── UQSH_CMB_Stacking.ipynb # Reconstruction notebook
├── README.md

├── UQSH_CMB/
│ ├── sparkling_voids.dat
│ ├── ergebnisse_final.txt
│ ├── plot_01_cmb.png
│ ├── plot_02_2mrs.png
│ ├── plot_03_stacking_final.png
│ ├── plot_05_sparkling_voids.png
│ └── COM_CMB_IQU-smica_2048_R3.00_full.fits

├── UQSH_CMB_v2/
│ ├── COM_CMB_IQU-143-fgsub-sevem_2048_R3.00_full.fits
│ ├── COM_CMB_IQU-217-fgsub-sevem_2048_R3.00_full.fits
│ └── results/
│ ├── plot_achromatisch.png
│ └── ergebnisse_achromatisch.txt


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

## License

MIT License
