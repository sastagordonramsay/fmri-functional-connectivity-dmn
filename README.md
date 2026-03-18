ROI-Based Functional Connectivity Analysis of Resting-State fMRI

Overview

This project implements an ROI-based functional connectivity analysis pipeline using resting-state fMRI data. The analysis demonstrates how 4D neuroimaging data can be transformed into interpretable brain networks using Python-based tools.

Objectives

Process 4D fMRI data into analyzable time-series

Extract region-wise signals using anatomical atlases

Compute functional connectivity between brain regions

Visualize network structure using heatmaps and connectome plots

Dataset

Source: Nilearn developmental fMRI dataset

Type: Resting-state fMRI

Format: NIfTI (.nii.gz)

Dimensions: 4D (x, y, z, time)

Methods

1. Preprocessing

Temporal filtering (0.01–0.1 Hz)

Detrending

Standardization (z-score normalization)

Brain masking using NiftiMasker

2. ROI Extraction

Atlas: Harvard-Oxford cortical atlas

ROI time-series extracted using NiftiLabelsMasker

3. Connectivity Analysis

Pearson correlation between ROI time-series

Generation of connectivity matrix

Results

Functional Connectivity Heatmap

Brain Network Visualization

Key Findings
Moderate to strong positive correlations between selected brain regions

Evidence of hub-like connectivity patterns in specific ROIs

Network structure consistent with resting-state functional organization

Tools & Libraries

Python

Nilearn

Nibabel

NumPy

Matplotlib

Seaborn

How to Run
pip install -r requirements.txt

jupyter notebook dmn_analysis.ipynb

### Limitations
- Single-subject analysis
- Simplified preprocessing (no confound regression)
- Approximate ROI selection for DMN
  
Notes
This analysis provides an approximate ROI-based representation of resting-state networks and is intended as a demonstration of computational neuroimaging workflows. This analysis is performed on a single subject as a proof-of-concept for pipeline implementation.
