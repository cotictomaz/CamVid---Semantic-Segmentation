# Semantic Segmentation on CamVid

This project performs semantic segmentation on the CamVid dataset — a benchmark for autonomous driving scene understanding. The dataset used is slightly different from the original CamVid, with a different train-test split.

---

## 🚀 Project Overview

Implemented and compared some traditional segmentation models:

- Classical U-Net
- U-Net with ResNet backbones (ResNet-34, ResNet-50, ResNet-101)
- DeepLabV3+ with ASPP and dilated convolutions

Goals: 
- Evaluate how architecture and backbone depth affect segmentation quality.
- Evaluate how useful pretrained backbones are.
- Effect of Focal loss.

---

## 📂 Dataset — CamVid

| Property | Details |
|---------|---------|
| Domain | Road scenes / Autonomous driving |
| Labels | Pixel-wise semantic segmentation classes |
| Data split | 500/100/100 |

---

## 📊 Results — Summary

| Model | Backbone | Notes |
|------|----------|------|
| U-Net | ResNet-50 | ⭐ Best overall performance |
| U-Net | ResNet-34 / ResNet-101 | Higher capacity → improved results |
| DeepLabV3+ | ResNet backbone | Improves with fine-tuning |

- Increasing model capacity improved segmentation accuracy  
- Pretrained backbone implementation significantly outperformed custom training  
- Class imbalance remains a major challenge. Adding weighted Focal loss doesn't improve results.  

---

## 🖼️ Detailed description

For a more comprehensive overview, please see the accompanying PowerPoint presentation.

