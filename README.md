VLF-EM Signal Anomaly Detection using EEMD
This project demonstrates how to simulate and analyze a Very Low Frequency Electromagnetic (VLF-EM) signal using Empirical Ensemble Mode Decomposition (EEMD) to detect anomalies — such as mineral deposits or resource irregularities — along a survey line.

Overview
This process applies to geophysical exploration problems where VLF-EM data is used to detect subsurface conductive anomalies. By decomposing a signal into Intrinsic Mode Functions (IMFs) using EEMD, we can isolate and identify outliers that may indicate:

Conductive ore bodies

Water tables

Structural disruptions (faults/fractures)

Equipment or survey errors

Features
Synthetic VLF-EM signal generator

EEMD decomposition using PyEMD

IMF visualization

Signal reconstruction & noise filtering

Anomaly detection using residual thresholding

Files
File	Description
eemd_anomaly_detection.py	Main script to simulate, decompose, and detect anomalies
README.md	This documentation
requirements.txt	Python dependencies

Example Output
Plot of raw VLF-EM signal with anomaly

IMF decomposition plots

Residual plot with anomalies highlighted

Console printout of detected anomaly locations

Requirements
Python 3.7+

NumPy

Matplotlib

PyEMD (pip install EMD-signal)

Installation
bash
Copy
Edit
git clone https://github.com/yourusername/vlf-em-eemd-anomaly.git
cd vlf-em-eemd-anomaly
pip install -r requirements.txt
▶️ Usage
bash
Copy
Edit
python eemd_anomaly_detection.py
This will:

Simulate a VLF-EM signal with an embedded deposit anomaly.

Apply EEMD decomposition.

Reconstruct the denoised signal.

Highlight anomalies in the residual signal.

How It Works
Simulate a geophysical line profile with:

Natural geologic background (sinusoid)

Gaussian anomaly (deposit)

Random noise

Decompose signal using EEMD into multiple IMFs:

IMF1 = high-frequency noise

IMF2–n = structure, trend

Reconstruct the denoised signal by summing IMF2 and onward.

Detect anomalies by thresholding the residual (original - reconstructed).

Applications
Mineral exploration

Environmental surveys

Infrastructure planning

Subsurface anomaly mapping

📬 Contact
Created by Alaedin E.
