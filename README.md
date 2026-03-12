# 🖊️ ICDAR 2026 — Pen Classification

EfficientNet-B0 transfer learning pipeline for the **ICDAR 2026 CircleID Pen Classification** Kaggle competition.  
Classifies handwriting tool images into **8 pen categories** with full training visualization suite.

## 📁 Project Structure
```bash
├── pen-classification.ipynb   # Main notebook
├── requirements.txt
└── README.md
```
## 🚀 Quickstart
pip install -r requirements.txt

## 🧠 Model
- **Architecture:** EfficientNet-B0 (pretrained on ImageNet via timm)
- **Classes:** 8 pen types (pen_id 1–8)
- **Input size:** 224×224

## ⚙️ Training Details
| Parameter | Value |
|---|---|
| Optimizer | AdamW (lr=1e-3, wd=1e-4) |
| Scheduler | ReduceLROnPlateau (factor=0.5, patience=2) |
| Batch size | 128 |
| Max epochs | 30 |
| Early stopping | patience=5 |
| Augmentations | HFlip, VFlip, Rotation±20°, ColorJitter |

## 📊 Visualizations
1. Class Distribution (bar + pie)
2. Train/Val Split per class
3. Sample images per class
4. Augmentation preview
5. Model architecture diagram
6. Training curves (loss, accuracy, LR)
7. Confusion matrix
8. Per-class accuracy
9. Correct vs incorrect prediction grid
10. Test set prediction distribution

## 📤 Output
Generates `submission_pen.csv` ready for Kaggle submission.

## 🔗 Competition
[ICDAR 2026 CircleID Pen Classification](https://www.kaggle.com/competitions/icdar-2026-circleid-pen-classification)
