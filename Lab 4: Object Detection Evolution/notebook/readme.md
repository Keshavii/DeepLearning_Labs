# Object Detection Pipeline: From R-CNN to YOLO

**Name:** Hiya Modi 
**ID:** 202301011

---

## Overview

This project implements and analyzes the evolution of object detection models, progressing from classical region-based methods (R-CNN) to modern real-time detectors (YOLOv8). The objective is to understand how computational inefficiencies are progressively eliminated through architectural innovations.

The lab covers the complete detection pipeline, including ground truth visualization, overlap metrics, region proposal methods, deep feature extraction, optimization techniques, and end-to-end object detection.

---

## Tasks Implemented

### Task 0: Ground Truth Visualization
- Parsed Pascal VOC XML annotations
- Visualized bounding boxes and class labels

### Task 1: Intersection over Union (IoU)
- Implemented IoU from scratch
- Validated across multiple overlap scenarios

### Task 2: Selective Search
- Generated approximately 1800 region proposals
- Selected top 200 proposals for further processing

### Task 3: R-CNN Bottleneck
- Processed each region independently using ResNet18
- Demonstrated computational inefficiency

### Task 4: Fast R-CNN (RoI Pooling)
- Shared feature extraction across regions
- Achieved significant speedup compared to R-CNN

### Task 5: Faster R-CNN
- Used Region Proposal Network (RPN)
- Performed end-to-end object detection

### Task 6: Non-Maximum Suppression (NMS)
- Implemented custom NMS using IoU
- Removed redundant overlapping detections

### Task 7: YOLO Fine-Tuning
- Fine-tuned YOLOv8 Nano model
- Evaluated performance using mAP metrics

---

## Results Summary

| Model                      | Inference Time (ms/img) | mAP@50 | mAP@50-95 |
|---------------------------|------------------------|--------|-----------|
| Faster R-CNN (pretrained) | 7513.78                | N/A    | N/A       |
| YOLOv8 (pretrained)       | ~95                    | 0.75   | 0.55      |
| YOLOv8 (fine-tuned)       | 93.6                   | 0.831  | 0.627     |

---

## Key Observations

- R-CNN suffers from redundant computation due to repeated CNN passes.
- Fast R-CNN eliminates this by sharing feature maps, resulting in a significant speed improvement.
- Faster R-CNN introduces learned region proposals through the Region Proposal Network (RPN).
- YOLO removes the region proposal stage entirely and performs detection in a single forward pass.
- Fine-tuning YOLO improves detection performance by adapting the model to dataset-specific features.

---

## Key Insights

- There is a clear trade-off between accuracy and computational efficiency.
- Eliminating redundant operations is critical for scaling object detection models.
- End-to-end learning architectures outperform traditional multi-stage pipelines.

---

## Technologies Used

- Python  
- PyTorch / Torchvision  
- OpenCV  
- Matplotlib  
- Ultralytics YOLOv8  

---

## Conclusion

This project demonstrates the evolution of object detection systems from computationally expensive, multi-stage pipelines to efficient, real-time models. The results highlight the importance of eliminating redundant computation and adopting end-to-end learning frameworks.

Among all approaches, YOLO (fine-tuned) provides the best balance between speed and accuracy for practical applications.

---
