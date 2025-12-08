# YOLO-MT-A-Lightweight-Multi-Task-Learning-Framework-

You can find the inference and training code from bdd100k.ipynb notebook.

- **Hugging Face:** https://huggingface.co/kursatkomurcu/YOLO-MT-A-Lightweight-Multi-Task-Learning-Framework  

# 🚗 YOLO-MT: Lightweight Multi-Task Learning for Unified Scene Understanding

YOLO-MT is a **YOLOv12-based lightweight multi-task learning framework** that performs **object detection, lane detection, drivable area segmentation, and scene attribute classification** within a single unified model.  
It is specifically designed for **real-time autonomous driving and embedded systems** with limited computational resources.

## ✨ Key Features
- ✅ **4 tasks in a single network**
  - Object Detection  
  - Lane Detection  
  - Drivable Area Segmentation  
  - Scene Attribute Classification (weather, scene type, time of day)
- ⚡ **Real-time inference**
- 📦 **Only 2.9M parameters**
- 🧠 **Shared YOLOv12 backbone**
- 🔥 Optimized for **embedded and edge devices**
- 📊 Trained and evaluated on the **BDD100K dataset**

## 🏗️ Architecture Overview
- Shared **YOLOv12 encoder**
- Lightweight **multi-branch decoder**
- **ASPP-Lite** module for context aggregation
- Separate task-specific heads for:
  - Lane segmentation
  - Drivable area segmentation
  - Attribute classification

## 🎯 Training Strategy
1. Train YOLOv12 on **object detection**
2. **Freeze the backbone**
3. Jointly train:
   - Lane detection  
   - Drivable area segmentation  
   - Attribute classification  

This two-stage training ensures **strong feature reuse** while keeping the model extremely compact.

## 📁 Dataset
- **BDD100K**
  - Object detection annotations
  - Lane markings
  - Drivable area masks
  - Scene attributes (weather, scene type, time of day)

All images are resized to **384×640** for efficient real-time processing.

## 📌 Use Cases
- Autonomous driving perception
- Advanced Driver Assistance Systems (ADAS)
- Embedded AI systems
- Edge deployment for robotics

---

## Example outputs
![example](https://github.com/kursatkomurcu/YOLO-MT-A-Lightweight-Multi-Task-Learning-Framework-/blob/main/multitasking_example.png)

