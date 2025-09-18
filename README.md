# VideoTransformer-Adversarial-XAI

This repository contains the implementation of methods and analysis tools described in our paper on adversarial attacks and XAI analysis for transformer-based video models.

## Overview

This repository provides a comprehensive implementation of various adversarial attack methods targeting video transformer models, along with explainable AI (XAI) tools for analyzing the impact of these attacks on spatiotemporal attention patterns. The code supports reproducibility of our experimental results and facilitates future research in video model robustness.

## Repository Structure

The repository is organized into separate directories for each attack method, with implementations provided as Jupyter Notebooks (.ipynb):

- `SpatioTemporalAttack/`: Our novel joint spatiotemporal attack method that specifically targets video transformer attention mechanisms
- `Frame-WiseAttack/`: Implementation of traditional frame-wise attacks that apply perturbations to each frame independently
- `SparseOpticalFlowAttack/`: Optical flow-guided sparse attack method that selectively perturbs key frames
- `V-BAD/`: Implementation of the V-BAD black-box attack method
- `CCB_Attackk/`: Tools for applying common corruptions (Gaussian noise, motion blur, etc.) to video data

## Attack Methods

### Joint Spatiotemporal Attack

Our proposed method that synchronizes perturbation generation across precise multi-frame temporal windows matching the video transformer's native temporal attention mechanisms. This approach directly manipulates the transformer's integrated spatiotemporal features through gradient computations.

### Frame-wise Attack

Traditional approach that applies adversarial perturbations to each frame independently. This serves as a baseline method to compare against more sophisticated approaches.

### Sparse Attack

An optical flow-guided approach that identifies and perturbs only key frames in the video sequence. This method reduces computational overhead while maintaining temporal attack effectiveness.

### V-BAD Attack

A state-of-the-art black-box attack method that combines transferable perturbations from image models with partition-based gradient estimation.

### Common Corruptions

Implementation of standard corruption types (Gaussian noise, shot noise, motion blur, zoom blur) based on the Common Corruption Benchmark to evaluate model robustness.

## Usage

Each attack method folder contains Jupyter notebooks that can be run interactively:

```bash
# Start Jupyter notebook server
jupyter notebook
```

Data Preparation

Some notebooks may require pre-processed video data or pre-trained models. Refer to the instructions in each notebook for specific data preparation steps. We also provide DataExamples.

## Citation

If you use this code in your research, please cite our paper:

@article{10.1145/3766071,
author = {Wang, Zerui and Liu, Yan},
title = {Joint Spatiotemporal Adversarial Attacks on Video Transformer Models Through XAI-guided Perturbation},
year = {2025},
publisher = {Association for Computing Machinery},
issn = {1551-6857},
url = {https://doi.org/10.1145/3766071},
doi = {10.1145/3766071},
journal = {ACM Trans. Multimedia Comput. Commun. Appl.}
}
