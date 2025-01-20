# Semantic-Segmentation-of-Underwater-Imagery
A segmentation project done as the final project of the Machine Learning for Computer Vision course at ESILV

A detailed presentation can be found in this repo at [Project_presentation.pdf](https://github.com/MikeCheek/Semantic-Segmentation-of-Underwater-Imagery/blob/main/Project_presentation.pdf)

## Example of output

![Example of trained model](./video/segmented.gif)

# Introduction

## What is Semantic Segmentation?
- **Definition:** Label each pixel of an image with a class/category.
- **Objective:** Segment underwater images into objects (e.g., fish, reefs, plants).
- **Goal:** Automatically label each pixel for underwater imagery analysis.

---

# Problem Statement

## Illustration of the Problem
- Challenges in segmenting underwater imagery.
- Importance of precise segmentation in marine applications.

---

# Project Goals

- Train a segmentation model to identify underwater objects.
- Generate segmentation masks with pixel-wise classification.

---

# Dataset Overview

## Structure
- **Train/Validation:** 1525 paired samples.
- **Test:** 110 paired samples for benchmarking.

## Object Categories
| Category          | RGB Code |
|-------------------|----------|
| Fish              | Yellow: 110 |
| Reefs             | Pink: 101 |
| Aquatic Plants    | Green: 010 |
| Wrecks/Ruins      | Sky: 011 |
| Human Divers      | Blue: 001 |
| Robots            | Red: 100 |
| Sea-floor         | White: 111 |
| Background        | Black: 000 |

# Methodology

## Segmentation Model
- **Model:** U-Net architecture.
- **Enhancements:** Dropout layers to prevent overfitting.

## Data Augmentation
- Techniques: Horizontal flipping, rotation, Gaussian noise, etc.

---

# Training Details

## Metrics
- **Dice Loss:** Measures overlap between predicted and ground truth masks.
- **IoU:** Evaluates the intersection over union for object regions.

## Optimizer & Scheduler
- **Adam Optimizer:** Learning rate = 1e-4.
- **Scheduler:** Reduces learning rate when validation loss plateaus.

---

# Results

## Training & Validation Loss
- Steady decline over 50 epochs.
- Minimal gap between training and validation loss.

## IoU Metrics
- Significant improvement in training and validation IoU.


# Future Directions

- **Hyperparameter Tuning:** Optimize learning rates and batch sizes.
- **Dataset Expansion:** Incorporate similar datasets.
- **Transfer Learning:** Use pretrained models for better feature extraction.
- **Advanced Augmentation:** Focus on underrepresented classes.

---

# Applications

- **Marine Ecology:** Track underwater species.
- **Archaeology:** Identify submerged historical sites.
- **AUVs:** Enhance underwater navigation.
- **Environmental Monitoring:** Assess vegetation health and pollution.

---

# Thank You!
