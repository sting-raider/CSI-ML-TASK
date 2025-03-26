# CSI-ML-TASK

## Overview
This project implements an advanced signature forgery detection system using machine learning techniques, combining feature extraction, style transfer, and classification to analyze and identify forged signatures.

## Key Components

### 1. Feature Extraction
The project uses two advanced feature extraction techniques:
- Histogram of Oriented Gradients (HOG)
- Local Binary Pattern (LBP)

These features are extracted from signature images to capture unique characteristics that distinguish real and forged signatures.

### 2. Machine Learning Classifier
A Support Vector Machine (SVM) with RBF kernel is trained to classify signatures:
- Trained on a dataset of real and forged signatures
- Achieves high accuracy (98% in testing)
- Provides probability scores for classification

### 3. Synthetic Forgery Generation
Utilizes Neural Style Transfer (NST) to generate synthetic forged signatures:
- Uses a pre-trained VGG19 model
- Applies artistic styles to original signatures
- Allows controlled generation of synthetic forgeries

## Project Workflow

1. **Data Preparation**
   - Load signature images from `signature_dataset`
   - Separate real and forged signatures

2. **Feature Extraction**
   - Convert images to grayscale
   - Resize and apply Gaussian blur
   - Extract HOG and LBP features

3. **Model Training**
   - Split data into training and testing sets
   - Train SVM classifier
   - Save trained model for future use

4. **Synthetic Forgery Generation**
   - Use Neural Style Transfer to create synthetic forged signatures
   - Apply artistic styles from ArtBench10 dataset
   - Generate controlled number of forgeries

5. **Forgery Evaluation**
   - Classify generated forgeries
   - Provide prediction and probability scores

## Requirements
- requirements.txt