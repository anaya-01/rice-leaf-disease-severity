# Rice Leaf Disease Severity Analysis

This repository contains the code developed for the study **“Comparing Lesion Severity Across Rice Leaf Diseases Using Image-Based Quantification.”**

The study investigates differences in image-derived severity estimates across ten rice leaf disease classes using a DenseNet-121 classification model and Grad-CAM-based image analysis.

## Motivation & Goals

Rice leaf diseases can produce different patterns and extents of visible tissue damage. This project explores whether these differences can be quantified consistently from rice leaf images.

The study aims to:

- classify rice leaf images across ten disease categories;
- identify image regions contributing to model predictions using Grad-CAM;
- derive an image-based severity score from high-activation regions within the visible leaf area; and
- compare severity estimates across disease categories using statistical analysis.

## Dataset

The study uses the **Paddy Doctor: Paddy Disease Classification** dataset.

The dataset contains 10,407 labeled rice leaf images across ten classes:

- Healthy leaves
- Leaf blast
- Brown spot
- Bacterial leaf blight
- Bacterial leaf streak
- Tungro
- Rice hispa
- Dead heart
- Downy mildew
- Bacterial panicle blight

The dataset was divided using an 80:20 split:

- **Training set:** 8,323 images
- **Held-out validation set:** 2,084 images

The validation images were not augmented or used during model training and were reserved for final evaluation and severity analysis.

## Methods Overview

### 1. Disease Classification

A **DenseNet-121** model initialized with ImageNet weights was fine-tuned to classify rice leaf images into the ten disease categories.

### 2. Grad-CAM Visualization

**Gradient-weighted Class Activation Mapping (Grad-CAM)** was applied to the trained model to identify image regions contributing to its predictions.

### 3. Image-Derived Severity Estimation

Grad-CAM activation maps were thresholded to generate binary high-activation masks.

Image-derived severity was calculated as the proportion of high-activation pixels within the segmented visible leaf area.

This produces a continuous severity score for each image while accounting for differences in visible leaf area.

### 4. Statistical Analysis

Severity estimates were compared across disease classes to investigate differences in their distributions.

The repository includes the code used for model training, Grad-CAM generation, severity extraction, and statistical analysis.

