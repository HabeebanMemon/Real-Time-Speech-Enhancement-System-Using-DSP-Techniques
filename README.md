# Real-Time-Speech-Enhancement-System-Using-DSP-Techniques
A high-performance Digital Signal Processing (DSP) solution designed to improve speech intelligibility by suppressing background noise in real-time audio streams.

**Overview*
This project implements a robust speech enhancement pipeline in Python. It is engineered to handle diverse noise profiles by dynamically estimating the noise floor and performing precise spectral subtraction in the frequency domain.

**Key Features*
Spectral Subtraction: Core algorithm used to attenuate noise by subtracting the estimated noise power spectrum from the noisy speech spectrum.

Automated Noise Gating: Effectively silences audio intervals where only noise is present, significantly improving overall clarity and perceived quality.

Butterworth Band-Pass Filtering: Removes out-of-band frequencies and unwanted artifacts while strictly preserving the human speech frequency range.

SNR Analysis: Automatically calculates and compares the Signal-to-Noise Ratio (SNR) of original vs. enhanced audio to provide a quantitative performance metric.

Visualizations: Generates high-fidelity Time-Domain Waveforms and Spectrograms for visual verification of noise reduction.

*Technical Implementation*
The system follows a modular DSP architecture to ensure computational efficiency and signal accuracy:

Audio Preprocessing: Implements framing and windowing (Hamming window) using the Short-Time Fourier Transform (STFT).

Noise Estimation: Continuous estimation of background noise levels during initial speech pauses to build a reliable noise profile.

Enhancement Pipeline: Sequential application of spectral subtraction and noise gating to clean the signal.

Reconstruction: Converting the processed signal back to the time domain using the Inverse STFT (ISTFT) and the overlap-add method.

*Evaluation & Results*
The system's performance is validated through a three-tier analysis:

Waveform Comparison: Visualizes the reduction in "thick" noise bands and the preservation of speech transients in the time domain.

Spectrogram Analysis: Demonstrates the surgical removal of constant-frequency noise, broadband hiss, and electrical hum.

SNR Metrics: Provides a concrete decibel (dB) improvement score for every processed file, confirming successful enhancement.

*Dependencies*
Python 3.x

NumPy & SciPy: Core signal processing and matrix mathematics.

Librosa: Specialized audio analysis and feature extraction.

Matplotlib: Advanced data visualization and plotting.

SoundFile: High-quality audio I/O handling.

*Contributors*
Developed by: Habeeban Memon

Academic Supervision: Engr. Asif Ali (Sukkur IBA University)
