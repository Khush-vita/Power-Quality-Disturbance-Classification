# Interpretable Power Quality Disturbance Classification using MIL

Developed a Multi-Instance Learning (MIL) framework for automatic power quality disturbance classification using Zenodo benchmark datasets.

## Dataset
- 17 Power Quality Disturbance Classes
- 1000 signals per class
- 100 samples per signal

## Key Features
- 4-channel signal representation:
  - Raw Signal
  - FFT Spectrum
  - Harmonic Profile
  - Hilbert Envelope
- 1D CNN-based feature extraction
- Attention-based MIL architecture
- Overlapping window segmentation (window size = 50, stride = 25)
- Attention-based disturbance localization
- AdamW optimizer for model training

## Pipeline
Signal → Windows → CNN → Attention → Classification

## Supervisors
- Dr. Vivek Kanhangad
- Dr. Dibbendu Roy
