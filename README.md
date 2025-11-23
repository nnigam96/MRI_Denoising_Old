# MRI Denoising - Legacy Implementation

A PyTorch Lightning-based implementation for automatic bias field correction and denoising of Magnetic Resonance Imaging (MRI) scans using deep learning. This repository contains the original capstone project implementation with UNet architectures.

## Problem Statement

MRI scans suffer from two primary artifacts:
- **Noise**: Random fluctuations that degrade image quality
- **Bias Fields**: Low-frequency intensity non-uniformities caused by magnetic field inhomogeneities

This project addresses both issues using deep learning approaches, including UNet architectures and CycleGAN-based methods.

## Features

- **PyTorch Lightning**: Structured training framework with automatic checkpointing
- **UNet Architecture**: 2D/3D UNet for denoising tasks
- **CycleGAN Approach**: Alternative implementation for unsupervised domain adaptation
- **Bias Field Correction**: Integration of N4 bias field correction
- **Jupyter Notebooks**: Interactive exploration and visualization

## Project Structure

```
MRI_Denoising_Old/
├── train_unet.py          # Main UNet training script (PyTorch Lightning)
├── lightning_unet.py       # Lightning module definition
├── mri_sup_dataset.py     # Dataset loading and preprocessing
├── unet.py                # UNet architecture
├── CycleGAN_Approach/     # Alternative CycleGAN implementation
└── notebooks/             # Jupyter notebooks for analysis
```

## Technical Details

### Architecture

- **Model**: UNet with configurable 2D/3D spatial dimensions
- **Framework**: PyTorch Lightning for structured training
- **Loss Function**: MSE or other configurable losses
- **Preprocessing**: N4 bias field correction, intensity normalization

### Training

The training pipeline includes:
- Automatic validation monitoring
- Model checkpointing
- Loss curve visualization
- Test set evaluation

## Quick Start

### Prerequisites

```bash
pip install torch pytorch-lightning monai
```

### Training

```bash
python train_unet.py
```

### Interactive Exploration

Use the Jupyter notebooks in the `notebooks/` directory for data exploration and visualization.

## Capstone Project

This was developed as part of ECE697 (Capstone Course Project) by Cameron Craig and Justin Hiemstra, with contributions and extensions for MRI denoising research.

## License

See repository for license information.
---

This repository contains the codebase for our capstone course project. Some of the files here are python notebooks which were used to interactively explore data and develop various components of the project. The core code for training the supervised U-Net exists as multiple .py files.

### Usage:

Please run the notebook 'run_project_demo.ipynb' on Google Colab. You can access it  [here](https://colab.research.google.com/drive/1ojJ0Y0Ct1zwjKPgS643_Fxtlq-aTWUx7?usp=sharing).

This notebook contains an easy-to-use and step-by-step guide through the core functions of the codebase. It is intended to be run inside of Google Colab with a GPU runtime. It may work outside of colab on your local machine if your python environment is similar to the stock colab environment.
