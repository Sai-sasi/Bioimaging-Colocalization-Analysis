# Multi-Channel Confocal Colocalization Analysis
## ImageJ/FIJI — JACoP Plugin — Mouse Mesenteric Artery

**Author:** Sai Sasi Sekhar Kongala  
**Course:** BIOL5261 — Bio-Imaging for Research Scientists  
**Institution:** University of Glasgow, School of Life Sciences  
**Academic Year:** 2024–2025  
**Grade Awarded:** A5 (University of Glasgow Excellence Band)  

---

## Project Overview

This repository documents my formal assessed bioimaging analysis 
conducted as part of BIOL5261 at the University of Glasgow. I 
performed multi-channel merging and quantitative colocalization 
analysis on a 3-channel laser scanning confocal Z-stack of mouse 
mesenteric artery (MMA) tissue, investigating the spatial 
co-expression of adrenoceptor subtypes.

---

## Dataset Description

**Sample:** Mouse Mesenteric Artery (MMA)  
**Imaging System:** BioRad Radiance 2100 Laser Scanning Confocal  
**Format:** 3-channel confocal Z-stack (.pic format)  
**Dataset:** University of Glasgow course dataset — not publicly 
available (institutional data)

### Channel Assignment

| Channel | Fluorophore | Target | Colour |
|---------|------------|--------|--------|
| Channel 1 | QAPB | α1-adrenoceptors | Green |
| Channel 2 | CGP12177 | β-adrenoceptors | Red |
| Channel 3 | Syto 61 | Nuclear stain | Blue |

---

## Analysis Workflow

All analysis performed in **FIJI/ImageJ** using the **JACoP plugin** 
(Just Another Colocalization Plugin).

### Step 1 — Opening and Inspecting the Z-Stack
- Opened 3-channel Z-stack files (raw01, raw02, raw03)
- Verified channel integrity and Z-stack depth
- Confirmed correct channel-to-fluorophore assignment

### Step 2 — LUT Assignment
- Green LUT → QAPB (α1-adrenoceptors)
- Red LUT → CGP12177 (β-adrenoceptors)
- Blue LUT → Syto61 (nuclear marker)

### Step 3 — Multi-Channel Merging
- Merged all three channels into RGB composite
- Generated composite video for 3D Z-stack visualisation
- **Decision:** Skipped "Stack to Images" step to preserve 
  3D structure for colocalization analysis — collapsing to 
  2D slices would lose spatial information needed for 
  accurate JACoP analysis

### Step 4 — Colocalization Identification
- Identified yellow regions in composite = colocalization zones
- Yellow = green + red overlap = α1 and β receptor co-expression
- Colocalization most prominent at Z-slices 31–34

### Step 5 — JACoP Colocalization Analysis
Applied JACoP plugin to green (α1) vs red (β) channel pair:
- Pearson's correlation coefficient
- Costes' automatic threshold
- Mander's overlap coefficients
- Cytofluorogram analysis

### Step 6 — Correction Factor Assessment
- Evaluated whether correction factor (C) was applicable
- **Decision:** Not applicable — Dataset 3 contains a single 
  Z-stack with no paired secondary image for cross-validation
- Colocalization validity confirmed via Costes' threshold alone

---

## Results

### Quantitative Colocalization Metrics

| Metric | Value | Interpretation |
|--------|-------|---------------|
| **Pearson's Coefficient (r)** | **0.643** | Moderate-strong spatial overlap between α1 and β adrenoceptors |
| **Costes' Threshold (r)** | **0.538** | Statistically validates colocalization — not due to random signal |
| **Mander's M1** | **0.998** | Nearly all α1-adrenoceptor signal overlaps with β-adrenoceptor regions |
| **Mander's M2** | **0.929** | Strong reciprocal coverage — β signal broadly co-localises with α1 |

### Biological Interpretation

The high Mander's coefficients (M1 = 0.998, M2 = 0.929) combined 
with a moderate Pearson's r (0.643) suggest that while α1 and β 
adrenoceptors occupy largely the same spatial territory in the 
mesenteric artery wall, their intensity distributions are not 
perfectly correlated — consistent with differential expression 
levels at shared subcellular locations. This spatial co-expression 
raises the possibility of functional interaction or receptor 
heterodimerisation between adrenoceptor subtypes in vascular smooth 
muscle tissue.

---

## Analysis Summary Table

| Step | Completed | Notes |
|------|-----------|-------|
| Opened 3-channel Z-stack | ✅ | raw01 (green), raw02 (red), raw03 (blue) |
| Assigned correct LUTs | ✅ | Per fluorophore specification |
| Merged into RGB composite | ✅ | 3D composite + video |
| Identified colocalized regions | ✅ | Yellow zones at Z=31–34 |
| Stack to Images | ❌ Skipped | Preserved 3D structure intentionally |
| Applied JACoP plugin | ✅ | Green vs red colocalization |
| Pearson's correlation | ✅ | r = 0.643 |
| Costes' automatic threshold | ✅ | r = 0.538 |
| Mander's coefficients | ✅ | M1 = 0.998, M2 = 0.929 |
| Cytofluorogram | ✅ | Intensity correlation across Z-stack |
| Correction factor (C) | ❌ Not applicable | Single Z-stack — no paired dataset |

---

## Software and Tools

| Tool | Version | Purpose |
|------|---------|---------|
| FIJI/ImageJ | Latest | Image processing and analysis |
| JACoP Plugin | Standard | Colocalization quantification |
| BioRad Radiance 2100 | — | Original image acquisition |

---

## Files In This Repository

| File | Description |
|------|-------------|
| `README.md` | This file — full analysis documentation |
| `Bioimaging_Colocalization_Analysis_ImageJ_JACoP.pptx` | Original assessed presentation slides |

---

## Data Availability

The raw confocal Z-stack files (.pic format) are property of the 
University of Glasgow and are not publicly distributed. This 
repository documents the analytical methodology and results only.

For academic enquiries: sasisasisekhark@gmail.com

---

## Skills Demonstrated

`FIJI/ImageJ` `Confocal Microscopy` `Z-stack Analysis` 
`Multi-channel Merging` `LUT Assignment` `JACoP Plugin` 
`Colocalization Analysis` `Pearson Correlation` 
`Costes Thresholding` `Mander Coefficients` 
`Cytofluorogram Interpretation` `Fluorescence Microscopy` 
`Scientific Presentation` `Quantitative Image Analysis`

---

## Related Repositories

- [Electrophysiological-recordings](https://github.com/Sai-sasi/Electrophysiological-recordings) — 
  BBSRC-funded MSc dissertation: patch-clamp electrophysiology 
  R analysis and visualisation

---

*Part of an ongoing portfolio in computational neuroscience 
and bioimage analysis — building toward PhD research in 
translational pain neuroscience.*
