# Mosquito Species Detection using YOLOv8

A deep learning-based object detection model trained to identify multiple mosquito species from images using YOLOv8. The goal is to aid entomologists and public health professionals in quickly detecting mosquito types for better surveillance and disease prevention.

## Introduction

Mosquito-borne diseases continue to pose serious public health threats worldwide. Early identification of mosquito species is critical for monitoring and controlling their spread. This project leverages the YOLOv5 object detection framework to automate the detection and classification of six mosquito species from image data.

## Objective

- Build a lightweight and accurate object detection model for mosquito species.
- Enable fast inference on field-acquired images.
- Support real-world use in vector surveillance and research settings.

## Dataset

- Total Images: 946  
- Classes: 6 mosquito species  
- Each image contains bounding boxes and class labels for mosquito instances.
- Species Detected:
  - *Aedes aegypti*
  - *Aedes albopictus*
  - *Anopheles*
  - *Culex*
  - *Culiseta*
  - *Aedes japonicus / koreicus*

## Model

- Architecture: **YOLOv5** (Fused model, 72 layers)
- Parameters: ~3M  
- GFLOPs: 8.1  
- No gradient tracking during inference

## Evaluation Metrics

| Metric       | Value  |
|--------------|--------|
| Precision    | 0.545  |
| Recall       | 0.674  |
| mAP@0.5      | 0.644  |
| mAP@0.5:0.95 | 0.520  |

### Class-wise Performance:

| Class                  | Precision | Recall | mAP@0.5 | mAP@0.5:0.95 |
|------------------------|-----------|--------|---------|--------------|
| Aedes aegypti          | 0.722     | 0.486  | 0.625   | 0.548        |
| Aedes albopictus       | 0.693     | 0.914  | 0.868   | 0.683        |
| Anopheles              | 0.544     | 0.458  | 0.560   | 0.483        |
| Culex                  | 0.682     | 0.944  | 0.896   | 0.682        |
| Culiseta               | 0.375     | 0.711  | 0.605   | 0.488        |
| Japonicus/Koreicus     | 0.253     | 0.532  | 0.307   | 0.234        |

## Inference

The model can detect mosquito species in new images with bounding boxes and confidence scores. It's optimized for fast inference with minimal hardware requirements.

