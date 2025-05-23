# Tammathon Machine Learning Competition Solutions

This repository contains solutions for two tasks as part of the Tammathon Kaggle competition:

1. Cat Recognition Model (Task 1)
2. ICAO Photo Standards Compliance Classifier (Task 2)

## Task 1: Cat Recognition Model

A deep learning model to identify individual cats from images using state-of-the-art computer vision techniques.

### Dataset
- Training set: 405,033 images
- Validation set: 56,748 images
- Number of unique cat identities in training: 113,592
- Number of unique cat identities in validation: 16,425

### Implementation Details
- Framework: PyTorch
- Hardware: CUDA-enabled GPU
- Key Libraries:
  - torch & torchvision
  - timm (for model architectures)
  - albumentations (for image augmentation)
  - pandas & numpy (for data handling)
  - matplotlib (for visualization)

### Model Architecture
- Uses deep learning for feature extraction and classification
- Implements data loading optimization with DataLoader
- Employs GPU acceleration for faster training

## Task 2: ICAO Compliance Checker

A binary classification model to determine whether passport photos meet International Civil Aviation Organization (ICAO) standards.

### Dataset
- Training set: 3,978 images
- Validation set: 853 images
- Test set: 853 images
- Class distribution (Training):
  - Non-compliant (0): 3,800 images
  - Compliant (1): 178 images
  - Imbalance ratio: 21.35:1

### Implementation Details
- Model: EfficientNet B4 (tf_efficientnet_b4_ns)
- Input Image Size: 384x384
- Training Configuration:
  - Batch Size: 64
  - Learning Rate: 0.0001
  - Mixed Precision Training: Enabled
  - Number of Epochs: 30
  - Weight Decay: 1e-5

### Technical Features
- Mixed precision training for optimal GPU utilization
- Class weight balancing to handle imbalanced dataset
- Advanced data augmentation using Albumentations
- Hardware optimization for NVIDIA A100 GPU

## Setup and Installation

1. Clone the repository:
```bash
git clone https://github.com/[username]/Tammathon_Code.git
```

2. Install required packages:
```bash
pip install torch torchvision tqdm matplotlib scikit-learn pandas timm albumentations
```

3. Set up Kaggle credentials for data access:
```python
import kagglehub
kagglehub.login()
```

## Usage

Each task is implemented in a separate Jupyter notebook:
- Task 1: [`Cat_recognition.ipynb`](Cat_recognition.ipynb)
- Task 2: [`Compliance_check.ipynb`](Compliance_check.ipynb)

The notebooks can be run in Google Colab or any environment with GPU support.

## Model Performance

### Task 1: Cat Recognition
- Handles large-scale multi-class classification
- Optimized for identifying unique cat identities from images
- Uses advanced data augmentation for better generalization

### Task 2: ICAO Compliance
- Binary classification with class imbalance handling
- Specialized for passport photo compliance verification
- Implements weighted loss function to handle class imbalance

## Technical Requirements

- Python 3.11+
- CUDA-capable GPU
- Minimum 16GB RAM
- Storage space for datasets:
  - Task 1: ~39.1GB
  - Task 2: ~1.79GB

## License

This project is submitted as part of the Tammathon Kaggle competition. All rights reserved.