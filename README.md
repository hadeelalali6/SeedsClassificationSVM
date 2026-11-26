# Wheat Seeds Classification Using Kernel SVM

## Project Overview

This project implements a multiclass Support Vector Machine (SVM) with a Linear Kernel to classify wheat seeds based on their geometric characteristics.

The main objective is to implement and compare five optimization algorithms in terms of classification performance, convergence behavior, and computational efficiency.

## Dataset

- **Dataset:** Wheat Seeds Dataset
- **Number of Samples:** 210
- **Number of Features:** 7
- **Number of Classes:** 3
- **Task:** Multiclass Classification
- **Class Distribution:** Balanced (70 samples per class)

### Features

- Area
- Perimeter
- Compactness
- Length of Kernel
- Width of Kernel
- Asymmetry Coefficient
- Length of Kernel Groove

## Optimization Algorithms

1. Gradient Descent (GD)
2. Stochastic Gradient Descent (SGD)
3. Mini-Batch Gradient Descent
4. Adaptive Moment Estimation (Adam)
5. Root Mean Square Propagation (RMSprop)

## Methodology

- Data loading and inspection
- Data preprocessing
- Exploratory Data Analysis (EDA)
- Stratified train, validation, and test splitting
- Feature standardization
- Linear Kernel computation
- Multiclass SVM implementation
- Hinge Loss with L2 regularization
- Model training using five optimization algorithms
- Performance evaluation and comparison

## Experimental Configuration

| Parameter | Value |
|---|---|
| Kernel | Linear |
| Epochs | 200 |
| Learning Rate | 0.001 |
| Regularization Lambda | 0.01 |
| Random Seed | 42 |
| Training Set | 70% |
| Validation Set | 15% |
| Testing Set | 15% |

## Batch Size Configuration

| Optimizer | Batch Size |
|---|---:|
| Gradient Descent | 147 |
| Stochastic Gradient Descent | 1 |
| Mini-Batch Gradient Descent | 16 |
| Adam | 16 |
| RMSprop | 16 |

## Evaluation Metrics

- Accuracy
- Macro Precision
- Macro Recall
- Macro F1-Score
- Confusion Matrix
- Training Loss
- Validation Loss
- Test Loss
- Training Time
- Total Parameter Updates

## Project Structure

| Notebook | Description |
|---|---|
| 01_Gradient_Descent.ipynb | Gradient Descent implementation |
| 02_Stochastic_Gradient_Descent.ipynb | SGD implementation |
| 03_Mini_Batch_Gradient_Descent.ipynb | Mini-Batch GD implementation |
| 04_Adam.ipynb | Adam implementation |
| 05_RMSprop.ipynb | RMSprop implementation |

## Technologies and Libraries

- Python
- PyTorch
- NumPy
- Pandas
- Scikit-learn
- Matplotlib
- Seaborn
- Kaggle Notebooks

## Experimental Comparison

All optimization algorithms use the same dataset, data splits, feature scaling, kernel, loss function, and regularization coefficient.

The comparison focuses on classification performance, convergence stability, training time, and computational efficiency.

Although the number of epochs is fixed, the number of parameter updates differs depending on the batch size.
