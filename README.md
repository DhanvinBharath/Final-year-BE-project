Development of Robust Noise Reduction Techniques for Degraded Speech Enhancement.

A MATLAB-based speech enhancement framework designed to estimate and suppress background noise from degraded speech signals using statistical, spectral, and time-frequency noise-estimation techniques.

Overview
This project implements a complete offline speech enhancement pipeline. It corrupts clean speech with various real-world noise environments (e.g., babble, car, street, airport) using an additive noise model, transforms signals into the spectral domain via Short-Time Fourier Transform (STFT), estimates the noise spectrum using adaptive algorithms, and reconstructs enhanced speech using MMSE and Spectral Subtraction techniques.
Features
Degradation Modeling: Generates controlled degraded speech signals across multiple background noise types.

4 Noise Estimation Candidates:
IMCRA (Improved Minima Controlled Recursive Averaging)
MCRA (Minima Controlled Recursive Averaging)
SMPO (Soft-Mask Based Noise Estimation)
Conn_Freq (Connected Frequency/Time-Frequency Estimation)
Speech Enhancement: Employs MMSE spectrum power estimation and Spectral Subtraction (SP) to suppress estimated noise while preserving speech components.
Performance Evaluation: Automated generation of quantitative metrics (PESQ, NCM, SNR) and visual diagnostics (waveforms and spectrograms).
Tech Stack
Primary Environment: MATLAB
Core Processing: STFT / ISTFT, MMSE, Spectral Subtraction
Data Format: .wav audio files

Repository structure:

├── data/
│   ├── clean/        # Clean speech WAV inputs
│   ├── noise/        # Environmental noise WAV samples
│   └── degraded/     # Generated noisy speech outputs
├── src/
│   ├── estimation/   # IMCRA, MCRA, SMPO, Conn_Freq implementations
│   ├── enhancement/  # MMSE and Spectral Subtraction algorithms
│   └── utils/        # Preprocessing, STFT, and metrics calculations
├── results/          # Output audio files, PESQ/NCM metrics, and plots
└── main.m            # Pipeline execution script

Getting started
1. Clone the repository
2. Run in MATLAB
-Open MATLAB and set the project directory as your working folder.
-Ensure test audio files are present in the data/clean/ and data/noise/ directories.
-Run the execution scripts.
