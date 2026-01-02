# 🍀 Four-Leaf Clover Detection using YOLOv8

This project implements an object detection system to identify **four-leaf clovers** in images using **YOLOv8**.  
The goal is to detect and classify clovers as either **three-leaf** or **four-leaf**, enabling real-world applications such as mobile-based lucky clover finding.

---

##  Project Overview

- **Task**: Object Detection
- **Model**: YOLOv8 (Ultralytics)
- **Classes**:
  - clover-3
  - clover-4
- **Dataset Size**: ~1000 annotated images
- **Frameworks**: Python, Ultralytics YOLOv8, PyTorch
- **Deployment Target**: Mobile (Flutter via TFLite / ONNX in later versions)

---

##  Model Performance

| Metric | Value |
|------|------|
| Precision | ~77% |
| Recall | ~70% |
| mAP@50 | ~75% |
| mAP@50–95 | ~59% |

The model performs reliably despite class imbalance and is suitable for real-world experimentation.

##  Approach

1. Dataset sourced and preprocessed using Roboflow
2. Trained a YOLOv8 detection model
3. Evaluated performance using precision, recall, and mAP metrics
4. Prepared the model for future mobile deployment

---

##  Dataset Structure

dataset/
├── images/
│   ├── train/
│   └── val/
└── labels/
    ├── train/
    └── val/

##  Deployment

The trained YOLOv8 model was exported to **TensorFlow Lite (TFLite)** format for mobile deployment.  
This enables real-time inference in a Flutter-based mobile application.


## 🔄 Model Evolution

- **V1 – Image Classification**  
  A binary image classifier (3-leaf vs 4-leaf) was first developed to validate feature learnability and dataset quality (you can use the given dataset in the repo).

- **V2 – Object Detection (YOLOv8)**  
  The project was then extended to object detection to enable localization of clovers in real-world images, which is required for mobile and field-based use cases.
