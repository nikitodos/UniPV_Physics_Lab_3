# Physics Laboratory 3 – Optics, Lasers & Photonics
**University of Pavia · B.Sc. in Physics · A.Y. 2022–23**  
*Giovanni Nicola D'Aloisio*

> Experimental optics course covering LED/photodiode characterisation, laser diffraction,
> polarisation, optical activity, and light absorption.  
> All analysis notebooks are written in Python (Jupyter/Colab); raw data acquired with oscilloscopes
> and spectrometers and stored as CSV/XLSX.

---

## Repository structure

```
physics-optics-lab-3/
├── 01_LED_photodiode_DC/            ← I-V characteristic & DC coupling LED→PD
│   └── data/{part1, part2}/        ← Multimeter CSV at varying load resistances
├── 02_LED_photodiode_reverse/       ← Reverse-biased photodiode I-V
├── 03_LED_photodiode_AC/            ← Frequency response, bandwidth measurement
├── 04_LED_spectroscopy/             ← ⭐ LED electro-optical characterisation:
│   └── data/                           electric spectrum, optical spectrum, key parameters
│       ├── LED_ELECTRIC_SPECTRUM.CSV
│       ├── LED_OPTIC_SPECTRUM.CSV
│       └── LED_PARAMETERS.CSV
├── 05_lens_collimation_focusing/    ← Thin-lens equation, collimation of LED source
│   └── data/                        ← 3 collimation configs + no-lens reference + p-q pairs
├── 06_light_absorption/             ← Beer-Lambert law: 4 LED wavelengths × 3 filter colours
│   └── data/{LED_BLUE,GREEN,RED,YELLOW}/
├── 07_laser_diffraction/            ← ⭐⭐ HIGHLIGHT: single & double slit diffraction
│   ├── data/                            with red and green lasers; slit width inversion
│   │   ├── Diffraction.xlsx
│   │   └── LaserDiffraction.xlsx
│   ├── Notes.pdf                    ← Handwritten derivation notes
│   └── images/                      ← Diffraction pattern photos (JPG)
│       ├── Green/{Single, Double_A, Double_B}/   ← 5+4+3 images
│       └── Red/{Single, Double_A, Double_B}/     ← 5+4+3 images
├── 08_malus_law_and_wave_plates/    ← Malus's law + λ/4 and λ/2 wave-plate characterisation
├── 09_optical_activity/             ← Optical rotation in sugar solutions, Biot's law
└── 10_cosmic_rays/                  ← Bonus: Geiger counter coincidence measurement
    └── data/RawData.CSV
```

---

## Highlight: Laser diffraction (`07_laser_diffraction/`)

Single and double-slit diffraction patterns were photographed and quantitatively analysed for two laser wavelengths:

| Laser | λ | Slit configs | Images |
|---|---|---|---|
| Green diode | 532 nm | Single (5 widths) + Double A (4 spacings) + Double B (3 spacings) | 12 JPG |
| Red diode | 650 nm | Single (5 widths) + Double A (4 spacings) + Double B (3 spacings) | 12 JPG |

The notebook `Diffrazione da fenditura singola e doppia.ipynb` implements:
- Fraunhofer single-slit envelope fitting → slit width inversion
- Double-slit interference fringe spacing → slit separation
- Cross-validation between electric and optical measurements

---

## All experiments at a glance

| # | Experiment | Key physics | Instruments |
|---|---|---|---|
| 01 | LED-PD DC coupling | I-V curve, load line | Multimeter, variable R |
| 02 | Reverse-biased PD | Dark current, breakdown | Picoammeter |
| 03 | PD frequency response | Bandwidth, RC time constant | Function generator, oscilloscope |
| 04 | **LED spectroscopy** | **Bandgap, EL spectrum, optical spectrum** | **Spectrometer** |
| 05 | Lens collimation | Thin-lens equation, f-number | Optical bench, CCD |
| 06 | Light absorption | Beer-Lambert law, extinction coefficient | Photodiode, filters |
| 07 | **Laser diffraction** | **Fraunhofer diffraction, slit inversion** | **Laser, slits, CCD** |
| 08 | Malus's law + wave plates | Polarisation, birefringence | Polarisers, wave plates |
| 09 | Optical activity | Faraday rotation, Biot's law | Sugar solutions, polarimeter |
| 10 | Cosmic rays | Coincidence counting, Poisson statistics | Geiger-Müller tubes |

---

## How to run the notebooks

```bash
pip install numpy scipy matplotlib pandas openpyxl
jupyter notebook
```

Or open in [Google Colab](https://colab.research.google.com/).

---

## License

CC BY-NC-ND 4.0 · © 2023 Giovanni Nicola D'Aloisio
