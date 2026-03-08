# BoneFractureDetection

**📋 Overview**

A machine learning project that leverages YOLOv8 combined with SimCLR self-supervised pre-training to detect bone fractures in X-ray images. This hybrid approach enhances the model's ability to identify fractures with improved accuracy and robustness.

**🎯 Approach**

This project implements a two-stage training pipeline:

**Self-Supervised Pre-training (SimCLR)**

Pre-trains a YOLOv8 backbone using contrastive learning on unlabeled X-ray images. Learns meaningful feature representations without labeled data. Uses augmentations: random resized crops, horizontal flips, and rotations. 60 epochs of training with NT-Xent loss.

**Supervised Fine-tuning (YOLOv8)**

Fine-tunes the pre-trained backbone on labeled fracture detection data. Trains for 150 epochs with early stopping (patience=30). Uses advanced augmentations: mixup and label smoothing. Optimizes detection accuracy using YOLO's efficient architecture.

**🛠️ Technology Stack**

- Deep Learning Framework: PyTorch 2.9.0
- Object Detection: YOLOv8
- Self-Supervised Learning: SimCLR (custom implementation)
- Environment: Google Colab (T4 GPU)

**✨ Features**

- ✅ Hybrid Pre-training Strategy: Combines self-supervised and supervised learning
- ✅ SimCLR Implementation: Custom contrastive learning on medical imaging data
- ✅ Efficient Architecture: YOLOv8 nano model for fast inference
- ✅ Multi-level Evaluation: Train, validation, and test set metrics
- ✅ ONNX Export: Model exportable for production deployment
- ✅ Milestone Tracking: 4 milestone reports documenting progress
