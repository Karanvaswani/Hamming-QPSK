# Forward Error Correction in Digital Communications
### Hamming(15,11) Channel Coding + QPSK Modulation  
### with Image Transmission & Recovery over AWGN Channel

![Results](Project2_Hamming_QPSK_Results.png)

## Overview
A complete digital communication system simulator implementing the 
full transmit → encode → modulate → channel → demodulate → decode → 
receive chain. Demonstrates the power of Forward Error Correction (FEC) 
using Hamming(15,11) channel coding combined with Gray-coded QPSK 
modulation over an AWGN channel, including a visual image transmission 
and recovery demonstration.

## System Parameters
| Parameter | Value |
|---|---|
| Channel Code | Hamming(15,11) |
| Code Rate | 0.733 (11 data / 15 coded bits) |
| Error Correction | 1 bit per 15-bit codeword |
| Modulation | QPSK (Gray coded) |
| Bits per Symbol | 2 |
| Channel Model | AWGN |
| Image Demo Size | 64×64 pixels |

## Features
- **Hamming(15,11) encoder and decoder** with syndrome-based 
  single-bit error correction
- **Gray-coded QPSK modulator** and hard-decision demodulator
- **AWGN channel** simulation at configurable SNR levels
- **BER vs SNR Monte Carlo simulation** comparing:
  - Uncoded QPSK
  - Hamming-coded QPSK
  - Theoretical QPSK BER curve
- **Error correction counter** per SNR point
- **Image transmission demo** — transmit a 64×64 image through 
  the noisy channel and compare uncoded vs FEC-coded recovery
- **8-panel professional visualisation**

## BER Performance Results
| SNR (dB) | Uncoded BER | Hamming Coded BER | Improvement |
|---|---|---|---|
| 4 dB | 0.054 | 0.047 | 1.1x |
| 6 dB | 0.022 | 0.0077 | 2.9x |
| 8 dB | 0.0055 | 0.0011 | 5.1x |
| 10 dB | 0.0017 | ~0 | **17,000x** |

## How to Run
```bash
# Clone repository
git clone https://github.com/Karanvaswani/Hamming-QPSK-FEC-Communication-System
cd Hamming-QPSK-FEC-Communication-System

# Install dependencies
pip install -r requirements.txt

# Run simulation
python hamming_qpsk_system.py
```

## Concepts Demonstrated
- Hamming(15,11) linear block code encoding and decoding
- Syndrome-based single-bit error detection and correction
- Gray-coded QPSK modulation and coherent demodulation
- AWGN channel simulation and SNR calculation
- Forward Error Correction (FEC) coding gain analysis
- Shannon information theory and channel capacity
- BER performance comparison: coded vs uncoded systems
- Digital image transmission as a practical FEC demonstration
- Theoretical BER derivation using Q-function / erfc

## Tools & Technologies
Python | NumPy | SciPy | Matplotlib | Digital Communications |  
Information Theory | Forward Error Correction | Channel Coding

## Author
**Karan Kumar** — Electronics Engineer  
B.E. Electronic Engineering, Mehran University of Engineering & Technology  
IEEE Published Researcher (ICETECC 2025)  
GitHub: [Karanvaswani](https://github.com/Karanvaswani)  
LinkedIn: [karan-kumar-electronics-engineer](https://www.linkedin.com/in/karan-kumar-electronics-engineer/)

## License
MIT License — free to use for educational purposes.
