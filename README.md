# Real-Time-Speech-Enhancement-System-Using-DSP-Techniques

A Digital Signal Processing (DSP) solution to improve speech intelligibility by suppressing background noise in real-time audio streams.

##  Overview
This project implements a robust speech enhancement pipeline in Python. [cite_start]It is designed to handle various noise profiles by estimating the noise floor and subtracting it from the noisy signal in the frequency domain.



##  Key Features
* [cite_start]**Spectral Subtraction:** Core algorithm used to attenuate noise by subtracting the estimated noise power spectrum from the noisy speech spectrum.
* [cite_start]**Automated Noise Gating:** Effectively silences audio intervals where only noise is present, improving overall clarity.
* [cite_start]**Butterworth Band-Pass Filtering:** Removes out-of-band frequencies (noise) while preserving the human speech range.
* [cite_start]**SNR Analysis:** Automatically calculates and compares the Signal-to-Noise Ratio (SNR) of original vs. enhanced audio to quantify performance.
* [cite_start]**Visualizations:** Generates Time-Domain Waveforms and Spectrograms for visual verification of noise reduction.

##  Technical Implementation
The system follows a modular DSP architecture:
1. [cite_start]**Audio Preprocessing:** Framing and windowing using the Short-Time Fourier Transform (STFT).
2. [cite_start]**Noise Estimation:** Continuous estimation of background noise levels during speech pauses.
3. [cite_start]**Enhancement Pipeline:** Sequential application of spectral subtraction and noise gating.
4. [cite_start]**Reconstruction:** Converting the processed signal back to the time domain using Inverse STFT (ISTFT).


##  Evaluation & Results
The system's performance is validated through:
* [cite_start]**Waveform Comparison:** Visualizing the reduction in "thick" noise bands in the time domain.
* [cite_start]**Spectrogram Analysis:** Demonstrating the removal of constant-frequency noise and high-frequency hiss.
* [cite_start]**SNR Metrics:** Providing a concrete decibel (dB) improvement score for every processed file.

##  Dependencies
* Python 3.x
* [cite_start]NumPy & SciPy (Signal processing) 
* [cite_start]Librosa (Audio analysis) 
* [cite_start]Matplotlib (Visualization) 
* [cite_start]SoundFile (Audio I/O) 

---
[cite_start]**Developed by:** Habeeban Memon 
**Guided by:** Engr. [cite_start]Asif Ali (Sukkur IBA University)
