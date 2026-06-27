# Interpretable Power Quality Disturbance Classification using MIL

# Overview 
This project presents a deep learning framework for automatic classification of Power Quality Disturbances (PQDs) in electrical power systems.

The proposed system combines signal processing techniques with an Attention-Based Multiple Instance Learning (MIL) architecture to accurately classify disturbances while also identifying the most relevant signal region responsible for the prediction.

The model processes multiple representations of a power signal, including frequency-domain, harmonic, and envelope information, enabling robust disturbance recognition.


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
- Early stopping and learning-rate scheduling
- GPU acceleration with PyTorch

## Disturbance Classes
The model supports classification of:

1.Pure Sinusoidal
2.Sag
3.Swell
4.Interruption
5.Transient
6.Oscillatory Transient
7.Harmonics
8.Harmonics with Sag
9.Harmonics with Swell
10.Flicker
11.Flicker with Sag
12.Flicker with Swell
13.Sag with Oscillatory Transient
14.Swell with Oscillatory Transient
15.Sag with Harmonics
16.Swell with Harmonics
17.Notch

## Project Structure
Power-Quality-Classifier/
│
├── Dataset/                  # Disturbance datasets (CSV format)
├── ltspice_schematics/       # LTspice circuits used for waveform generation
├── models/                   # Saved trained models
│
├── main.py                   # Training, evaluation and localization pipeline
├── Demo.py                   # Demonstration/inference script
├── Presentation1.pdf         # Project presentation
└── README.md

## Methodology
1. Signal Acquisition
Power quality disturbance waveforms are generated using LTspice simulations and stored as CSV datasets.

2. Feature Extraction
Each signal is transformed into four complementary channels:

Channel 1: Normalized Time-Domain Signal
Captures waveform shape and amplitude variations.

Channel 2: FFT Magnitude Spectrum
Provides frequency-domain information useful for detecting harmonics and spectral distortions.

Channel 3: Harmonic Energy Profile
Extracts energy corresponding to harmonic frequencies, allowing direct analysis of harmonic contamination.

Channel 4: Hilbert Envelope
Uses the Hilbert Transform to obtain the instantaneous amplitude envelope, highlighting transient and modulation effects.

## Pipeline
Signal → Windows → CNN → Attention → Classification

## Supervisors
- Dr. Vivek Kanhangad
- Dr. Dibbendu Roy
