# CNN-Based Dental Disease Classification

This repository contains a deep learning project completed for an Applied Fundamentals of Deep Learning course at the University of Toronto in Spring 2025.

The goal of the project was to classify common oral diseases from real-world dental images using convolutional neural networks (CNNs). The system is intended as an assistive screening tool that could help improve access to preliminary dental assessments, particularly for underprivileged populations.

This was a team course project, and the report and code reflect collaborative development.

---

## Project Overview

The model predicts six classes:

- Caries  
- Calculus  
- Gingivitis  
- Tooth discoloration  
- Oral ulcers  
- Healthy  

Real-world intraoral images were collected from multiple public datasets. Because these images vary significantly in lighting, angle, and background, a substantial preprocessing pipeline was designed to improve robustness before training.

The project implemented:

- A traditional baseline model using HOG features + SVM  
- A primary CNN architecture trained end-to-end  
- Extensive image preprocessing and augmentation  
- Evaluation on held-out test data and unseen external datasets  

---

## Data Processing

Key preprocessing steps included:

- Noise reduction with OpenCV filters  
- Contrast mapping  
- Red channel enhancement to emphasize gum inflammation  
- Per-channel normalization  
- Data augmentation (rotation, cropping, flipping, blur, noise)  
- Stratified train/validation/test splitting  

Class imbalance was handled through augmentation and careful sampling.

---

## Models

### Baseline
- Histogram of Oriented Gradients (HOG)
- Support Vector Machine (SVM)

### CNN
- Multi-layer convolutional architecture with batch normalization  
- Fully connected layers with dropout  
- Adam optimizer  

Performance was further evaluated on unseen datasets to test generalization.

---

## Tech Stack

- Python  
- PyTorch  
- OpenCV  
- scikit-learn  
- NumPy / Matplotlib  
- Google Colab  

---

## Repository Contents

```
cnn_dental_classifier.ipynb
APS360_Final_Report.pdf
```

---

## Documentation

The full methodology, model architecture diagrams, preprocessing pipeline, evaluation protocol, and dataset sources are documented in:

```
APS360_Final_Report.pdf
```
