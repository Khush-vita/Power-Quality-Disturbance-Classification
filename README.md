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

## Pipeline
Signal → Windows → CNN → Attention → Classification

## Supervisors
- Dr. Vivek Kanhangad
- Dr. Dibbendu Roy
