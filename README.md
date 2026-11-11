# Tumor Detection in Low-Quality Radiology Images

**THE SOURCE CODE WILL BE ADDED TO THIS REPOSITORY AFTER THE PROJECT IS SUBMITTED.**

> 🚧 Work in progress · Supported by TÜBİTAK 2209-A

## What is this project?

Deep learning models for tumor detection are usually trained on clean, high-resolution images. Real clinical images are often noisy, low-contrast or low-resolution, and model accuracy drops on them.

This project tests whether **simple, fast image enhancement methods** (histogram equalization, CLAHE, median filtering) help a CNN detect tumors more reliably in low-quality radiology images, and which method helps most.

## How it works

```
low-quality MRI image
        │
        ▼
preprocessing (resize, normalize)
        │
        ▼
enhancement: histogram equalization │ CLAHE │ median filtering
        │
        ▼
CNN classifier (EfficientNet / ResNet, transfer learning)
        │
        ▼
tumor / no tumor  ──►  compared with the same model on original images
```

The models are compared with accuracy, precision, recall, F1-score and ROC-AUC.

## Tech stack

Python · PyTorch · OpenCV · NumPy · pandas · scikit-learn · Matplotlib · Jupyter · Google Colab

## Data

Public radiology datasets (e.g. Kaggle). Datasets are linked, not stored in this repository.

## Expected outputs

- Demo application that detects tumors in low-quality radiology images
- Comparison of enhancement methods with metrics and visualizations
- Preprocessed low-quality image set built from public data

## Related

- [BrainTumorClassification](https://github.com/esmadagdelen/BrainTumorClassification): my earlier CNN project for brain tumor classification on MRI images.
