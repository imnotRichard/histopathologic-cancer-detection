# Histopathologic Cancer Detection

## Overview

This repository contains code, analysis, and results for the Kaggle Histopathologic Cancer Detection competition.
The goal of this project is to develop a supervised learning model to identify metastatic cancer in small pathology image patches.

## Project Structure

- `histopathologic-cancer-detection.ipynb` — Main Jupyter notebook with all analysis, modeling, and results
- `my_submission.csv` — Submission file generated for the Kaggle competition
- `README.md` — Project overview and instructions

## Dataset

### Source: 
Kaggle Competition Data

### Content:

- `train/` - Training images (over 220,000 patches)

- `test/` - Test images for submission

- `train_labels.csv` - Ground truth labels for training images

- `sample_submission.csv` - Format for Kaggle submission

## Problem Statement

The objective is to classify whether the central 32x32 pixels of a 96x96 image patch contain metastatic cancer tissue.

This is a binary classification task:

- Label 1: Tumor tissue present

- Label 0: No tumor tissue

Submissions are evaluated using the Area Under the ROC Curve (AUC).

## Approach

The workflow for this project includes:

### 1.Exploratory Data Analysis (EDA):

- Visualizing sample images and label distribution

- Identifying class imbalance

### 2.Data Preprocessing:

- Image normalization and augmentation

- Train-validation split

### 3.Model Building:

- Simple Convolutional Neural Network (CNN)

- Transfer Learning with EfficientNetB0 (or other CNNs if pretrained weights are unavailable)

### 4.Model Evaluation:

- Performance metrics: Loss, Accuracy, AUC

- Training/validation curves

### 5.Submission:

- Generating and submitting predictions to Kaggle

- Leaderboard screenshot for result verification

## Results

Best public leaderboard AUC: 0.7963

## How to Reproduce

1.Download the competition dataset from Kaggle

2.Run the notebook histopathologic-cancer-detection.ipynb step by step

3.The submission file my_submission.csv will be generated at the end

## Notebooks and Scripts

histopathologic-cancer-detection.ipynb : Main notebook with code, comments, and explanations

## Acknowledgements

- The dataset and competition are hosted by Kaggle

- Dataset is based on the PatchCamelyon (PCam) benchmark:

  · Veeling et al., Rotation Equivariant CNNs for Digital Pathology, arXiv:1806.03962

  · Ehteshami Bejnordi et al., JAMA 2017, doi:jama.2017.14585
