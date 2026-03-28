# CKKS: A Step-by-Step Homomorphic Encryption Walkthrough

This repository is a hands-on exploration of the Cheon-Kim-Kim-Song (CKKS) scheme, a homomorphic encryption scheme for approximate arithmetic.

The main goal of the project is clarity: the notebook walks through the core CKKS ideas step by step, starting from encoding and decoding, then moving into encryption, decryption, and homomorphic operations.

It is based on the paper:

**Homomorphic Encryption for Arithmetic of Approximate Numbers**  
Jung Hee Cheon, Andrey Kim, Miran Kim, and Yongsoo Song  
Advances in Cryptology - ASIACRYPT 2017  
[Read the paper](https://eprint.iacr.org/2016/421.pdf)

## Why This Repo

- Learn CKKS through an interactive notebook rather than only theory
- See the full flow from vector encoding to encrypted computation
- Study exact polynomial arithmetic for ciphertext operations
- Compare the direct encoding method with an FFT-based alternative
- Use small toy examples that are easy to inspect and verify

## What You Will Find

### Main notebook

- [ckks.ipynb](./ckks.ipynb): the main tutorial notebook
- Covers encoding, decoding, encryption, decryption, addition, and multiplication
- Includes a step-by-step FFT alternative for encoding and decoding

### Supporting files

- [bfv_ckks.md](./bfv_ckks.md): additional notes and comparisons
- [mathematical_background.ipynb](./mathematical_background.ipynb): background material used by the main notebook

## Current Coverage

- [x] CKKS encoding and decoding
- [x] CKKS encryption and decryption
- [x] Homomorphic addition
- [x] Homomorphic multiplication tutorial example
- [x] FFT-based encoding and decoding alternative
- [ ] Integration with machine learning applications

## Quick Start

### 1. Create or activate the virtual environment

If you already have the included environment, activate it:

```bash
source myenv/bin/activate
```

### 2. Launch Jupyter

```bash
jupyter notebook
```

Then open [ckks.ipynb](./ckks.ipynb).

### 3. Run the notebook from top to bottom

The notebook is written as a guided walkthrough, so running cells in order will give the clearest explanation and the most consistent state.

## Project Focus

This repository is primarily educational.

That means the code favors readability and step-by-step explanation over production-grade optimization or cryptographic hardening. The examples use small parameters so the arithmetic is easy to follow.

## Notes

- CKKS works with approximate arithmetic, so decoded values are expected to be close to the original values rather than always exactly equal
- The notebook now includes an FFT-based view of encoding and decoding, which becomes much more important as the polynomial degree grows
- The multiplication section uses exact integer coefficient lists for ciphertext arithmetic so the algebra stays correct even when coefficients become large

## References

1. Jung Hee Cheon, Andrey Kim, Miran Kim, and Yongsoo Song  
   *Homomorphic Encryption for Arithmetic of Approximate Numbers*  
   Advances in Cryptology - ASIACRYPT 2017  
   [ePrint Archive](https://eprint.iacr.org/2016/421.pdf)

2. AI Tech Research Lab  
   *Introduction to BFV HE for ML*  
   [GitHub Repository](https://github.com/AI-Tech-Research-Lab/Introduction-to-BFV-HE-ML/blob/main/README.md)

3. Inferati Blog  
   *An Introduction to Fully Homomorphic Encryption and CKKS Scheme*  
   [FHE Schemes Overview](https://www.inferati.com/blog/fhe-schemes-ckks#sec-ckks-struct)

4. OpenMined Blog  
   *CKKS Explained: Part 1 - Simple Encoding and Decoding*  
   [CKKS Blog Post](https://blog.openmined.org/ckks-explained-part-1-simple-encoding-and-decoding/)

