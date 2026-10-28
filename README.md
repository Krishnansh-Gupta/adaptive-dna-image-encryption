# Adaptive DNA-Based Image Encryption with Feedback Diffusion

## Overview
This project implements a content-adaptive DNA-based image encryption method developed during an internship at the National Institute of Technology Delhi. The approach combines cryptographic key derivation, adaptive DNA coding, state-dependent permutation, chaotic sequence generation, DNA-XOR, feedback diffusion, and HMAC-SHA256 authentication to secure grayscale images.

## Key Features
- Content-adaptive encryption using image-derived descriptors.
- SHA-256-based cryptographic operations and secure key derivation.
- Eight DNA encoding rules using A, T, C, and G.
- State-dependent block permutation and Logistic chaotic sequences.
- Forward and backward ciphertext diffusion.
- HMAC-SHA256 authentication for detecting modified ciphertext.
- Encryption and decryption with exact image reconstruction.
- Security evaluation using entropy, pixel correlation, NPCR, UACI, key sensitivity, and plaintext sensitivity.
- Pixel2Noise analysis using controlled noise and data-loss experiments.
- Ablation studies to examine the contribution of individual encryption components.

## Experimental Setup
- **Dataset:** 49 grayscale images
- **Image dimensions:** 256 × 256 pixels
- **Block size:** 16 × 16 pixels
- **Implementation:** Python in Google Colab
- **Key techniques:** SHA-256, PBKDF2-HMAC-SHA256, HKDF-SHA256, Logistic map, DNA coding, and HMAC-SHA256

## Experimental Results
The method was evaluated on 49 valid grayscale images.

| Metric | Mean Result |
|---|---:|
| Ciphertext entropy | 7.997217 |
| NPCR | 99.610527% |
| UACI | 33.466698% |
| Horizontal correlation | 0.000304 |
| Vertical correlation | 0.000110 |
| Diagonal correlation | -0.000178 |
| Exact reconstruction | 49/49 images |

The average encryption time was approximately 0.853 seconds per image, and the average decryption time was approximately 0.862 seconds per image in the tested environment. These timings may vary with hardware and software configurations.

## Pixel2Noise Analysis
Salt-and-pepper noise, Gaussian noise, and data-loss experiments were performed on encrypted images. Modified ciphertexts were rejected by authentication checks in the tested cases. This demonstrates tamper detection under the evaluated conditions; it does not indicate that damaged ciphertext can be recovered automatically.

## Repository Structure
- `notebooks/` — Google Colab implementation
- `dataset/` — Input images (not included by default)
- `results/` — Encrypted images, decrypted images, and evaluation outputs
- `metrics/` — Security and performance measurements
- `README.md` — Project documentation

*The folder structure may be adjusted to match the files uploaded to this repository.*

## Purpose
The project aims to study DNA-based image encryption methods, compare their security and computational characteristics, and investigate content-adaptive encryption with feedback diffusion and ciphertext authentication.

## Disclaimer
The reported results are experimental and apply to the tested dataset and implementation. They should not be interpreted as a formal security proof or a guarantee of resistance to every cryptographic attack.

## Author
**Krishnansh Gupta**  
B.Tech. – Electronics and Communication Engineering  
National Institute of Technology Delhi

## Acknowledgment
This work was carried out during an internship at the National Institute of Technology Delhi under the guidance of Dr. Dharmendra Kumar Jharia.
