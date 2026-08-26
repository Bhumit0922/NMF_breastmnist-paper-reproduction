# BreastMNIST — Research Paper Reproduction

This repository contains my implementation and experimental reproduction
of a research paper using the BreastMNIST dataset.

## Overview

The project investigates the effect of dimensionality reduction on
deep image features for BreastMNIST classification.

The experimental pipeline consists of:

1. BreastMNIST dataset
2. Paper-faithful preprocessing
3. ResNet18 feature extraction
4. 512-dimensional feature representation
5. Dimensionality reduction to 30 dimensions
6. 5-NN classification
7. 10 experimental episodes
8. Evaluation using mean ± standard deviation

## Methods

The following representations were evaluated:

- Feature Space — 512D
- SVD — 30D
- NMF — 30D
- DNMF — 30D
- SCNMFS — 30D

## Experimental Settings

Two training/testing configurations were evaluated:

- 300 training / 80 testing
- 600 training / 160 testing

## Final Results

| Method | Dimension | 300/80 | 600/160 |
|---|---:|---:|---:|
| Feature Space | 512 | 76.50 ± 4.52 | 78.44 ± 3.48 |
| SVD | 30 | 77.75 ± 3.48 | 79.88 ± 3.36 |
| NMF | 30 | 73.25 ± 4.76 | 77.75 ± 3.43 |
| DNMF | 30 | 76.50 ± 5.13 | 78.88 ± 3.97 |
| SCNMFS | 30 | 67.88 ± 5.62 | 70.19 ± 2.95 |

## Best Method

SVD achieved the highest accuracy in both experimental settings:

- 300/80: 77.75%
- 600/160: 79.88%

## Dimensionality Reduction

Original feature dimension:

512

Reduced feature dimension:

30

Dimension reduction:

94.14%

## Paper Reproduction

The implementation was compared against the reported results from
the research paper.

The notebook reports:

- Absolute accuracy gap
- Relative accuracy gap
- Mean accuracy
- Standard deviation
- Improvement from 300/80 to 600/160

## Visualizations

The notebook includes visualizations for:

- Episode-wise accuracy
- Training-size effect
- Paper vs implementation
- Reproduction gap
- Accuracy distribution

## Environment

The experiments were performed using Kaggle with GPU acceleration.

Main libraries:

- PyTorch
- Torchvision
- NumPy
- Scikit-learn
- Matplotlib
- Pandas
- MedMNIST

## Notebook

The complete implementation is available in:

`notebooks/BreastMNIST_Paper_Implementation.ipynb`
