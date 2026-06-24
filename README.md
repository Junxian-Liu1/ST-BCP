# Improving Backward Conformal Prediction via Non-Conformity Score Transformation

This is the official implementation for the paper **["Improving Backward Conformal Prediction via Non-Conformity Score Transformation"](https://arxiv.org/abs/2602.01733)** at ICML 2026. It includes the complete pipeline for model training and the reproduction of all experimental results presented in the paper.

## Repository Structure

* **`train_main.ipynb`**: The complete training pipeline. It supports various architectures and benchmarks.
* **`STBCP.ipynb`**: Core implementation of the ST-BCP algorithm. This notebook generates all experimental data, figures, and tables used in the paper.

## Usage Guide

### 1. Model Training
Open `train_main.ipynb` to train the backbone models. 
* **Supported Models**: `ResNet-50`, `EfficientNet-B0`, `MobileNet-v3-small`, and `DenseNet-121`.
* **Supported Datasets**: `CIFAR-10`, `CIFAR-100`, and `TinyImageNet`.
* **Configuration**: You can easily switch between different model-dataset pairs by adjusting the parameters in the configuration cell.
* **Data Preparation**: Ensure the datasets are downloaded and the `dataset_path` is correctly set. Download links for the datasets are provided in the notebook comments.

### 2. Evaluation and Results
Open `STBCP.ipynb` to evaluate the framework and reproduce the paper's findings.
* **Prerequisites**: Before running, ensure that the required model weights are either:
    1.  Automatically exported to the `weights/` folder by running `train_main.ipynb`.
    2.  Manually downloaded and placed in the appropriate directory.
* **Output**: This script will compute the transformed non-conformity scores and generate result visualizations (saved in the `fig/` directory).
---
*Note: Directories for `weights/`, `logs/`, and `fig/` will be created automatically upon running the notebooks.*
