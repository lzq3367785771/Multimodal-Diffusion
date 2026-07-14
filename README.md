# StructureDiff: Multimodal Diffusion Learning for Neural Image Reconstruction

This repository contains the source code for the paper: *"Multimodal Diffusion Learning with Three-Dimensional Functional Magnetic Resonance Imaging Representation for Neural Image Reconstruction"*.

## Overview
StructureDiff is a multimodal diffusion-based model designed for natural image reconstruction from fMRI signals. Our approach preserves the 3D spatial structure of fMRI data using a Mamba-based architecture (fMRI-SSMNet) and introduces a dual-stream guidance mechanism (fMRI-SemBERT and fMRI-EdgeColorNet) to enhance detail accuracy, color fidelity, and semantic consistency.

## Prerequisites
- **Hardware**: Experiments were conducted on a workstation with two NVIDIA V100 GPUs.
- **Environment**: 
  - Python 3.x
  - PyTorch
  - (Please refer to `requirements.txt` for specific library versions)

## Datasets
To facilitate reproducibility while adhering to data privacy and size constraints, datasets should be prepared as follows:

### 1. Natural Scenes Dataset (NSD)
We utilize the **Natural Scenes Dataset (NSD)**. Due to the large size and license agreements of the NSD, we do not host the raw data in this repository.
- **How to obtain**: Please visit the [official NSD website](https://naturalscenesdataset.org/) to request access and download the raw fMRI data.
- **Preparation**: Ensure the dataset is preprocessed to 1.8 mm spatial resolution and includes the `flow` and `NSDGeneral` brain maps.
- **Placement**: Please place the downloaded data in the `./data/NSD/` directory.

### 2. ERGB Dataset (Self-built)
We introduce the **ERGB dataset**, which contains line art and color information to facilitate edge-color guidance during the reconstruction process.
- **Download**: You can download the preprocessed ERGB dataset and structural masks here: [[Link to Cloud Storage/Zenodo/Google Drive]]
- **Placement**: Please unzip the content into the `./data/ERGB/` directory.

