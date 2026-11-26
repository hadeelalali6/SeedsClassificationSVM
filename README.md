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
- Model training and optimization
- Performance evaluation
- Comparative analysis

## Experimental Configuration

| Parameter | Value |
|---|---|
| Kernel | Linear |
| Epochs | 200 |
| Learning Rate | 0.001 |
| Regularization Lambda | 0.01 |
| Random Seed | 42 |
| Training Samples | 147 |
| Validation Samples | 31 |
| Testing Samples | 32 |

## Batch Size and Parameter Updates

| Optimizer | Batch Size | Total Updates |
|---|---:|---:|
| GD | 147 | 200 |
| SGD | 1 | 29,400 |
| Mini-Batch GD | 16 | 2,000 |
| Adam | 16 | 2,000 |
| RMSprop | 16 | 2,000 |

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

## Experimental Results

### Classification Performance

| Optimizer | Train Accuracy | Validation Accuracy | Test Accuracy | Precision | Recall | F1-Score |
|---|---:|---:|---:|---:|---:|---:|
| GD | 91.84% | 83.87% | 87.50% | 87.50% | 86.97% | 86.80% |
| SGD | 93.20% | 87.10% | 87.50% | 87.50% | 86.97% | 86.80% |
| Mini-Batch GD | 91.16% | 83.87% | 87.50% | 87.50% | 86.97% | 86.80% |
| Adam | **93.88%** | **93.55%** | 87.50% | 87.50% | 86.97% | 86.80% |
| RMSprop | 91.16% | 90.32% | **90.63%** | **90.49%** | **90.30%** | **90.26%** |

### Loss and Training Efficiency

| Optimizer | Train Loss | Validation Loss | Test Loss | Training Time (s) |
|---|---:|---:|---:|---:|
| GD | 0.3032 | 0.3715 | 0.4366 | **0.5346** |
| SGD | 0.1945 | 0.2427 | 0.3082 | 22.6964 |
| Mini-Batch GD | 0.3031 | 0.3826 | 0.4292 | 2.1085 |
| Adam | **0.1745** | **0.2122** | **0.2755** | 2.3437 |
| RMSprop | 0.2574 | 0.3022 | 0.3326 | 2.0673 |

## Comparative Analysis

- **Gradient Descent:** Achieved the shortest training time and required the fewest parameter updates.
- **Stochastic Gradient Descent:** Achieved lower loss values than GD and Mini-Batch GD but required the longest training time.
- **Mini-Batch Gradient Descent:** Provided a balance between computational efficiency and classification performance.
- **Adam:** Achieved the highest validation accuracy and the lowest training, validation, and testing losses.
- **RMSprop:** Achieved the highest testing accuracy, precision, recall, and F1-score.

## Best Optimizers by Criterion

| Criterion | Best Optimizer |
|---|---|
| Highest Training Accuracy | Adam |
| Highest Validation Accuracy | Adam |
| Highest Testing Accuracy | RMSprop |
| Highest Precision | RMSprop |
| Highest Recall | RMSprop |
| Highest F1-Score | RMSprop |
| Lowest Training Loss | Adam |
| Lowest Validation Loss | Adam |
| Lowest Testing Loss | Adam |
| Fastest Training | GD |
| Fewest Parameter Updates | GD |

## Project Structure

| Notebook | Description |
|---|---|
| 01_Gradient_Descent.ipynb | Gradient Descent implementation |
| 02_Stochastic_Gradient_Descent.ipynb | SGD implementation |
| 03_Mini_Batch_Gradient_Descent.ipynb | Mini-Batch GD implementation |
| 04_Adam.ipynb | Adam implementation |
| 05_RMSprop.ipynb | RMSprop implementation |
| 06_Optimizers_Comparison.ipynb | Final performance comparison and analysis |

## Technologies and Libraries

- Python
- PyTorch
- NumPy
- Pandas
- Scikit-learn
- Matplotlib
- Seaborn
- Kaggle Notebooks

## Final Conclusion

The experimental results demonstrate that optimization algorithms differ in classification performance, convergence behavior, and computational efficiency.

RMSprop achieved the highest testing accuracy of 90.63% and the highest macro F1-score of 90.26%.

Adam achieved the highest validation accuracy of 93.55% and the lowest loss values across all three data subsets.

Gradient Descent achieved the fastest training time, while SGD required the highest computational time and number of parameter updates.

Based on validation performance, Adam is the preferred optimizer under the current experimental configuration.

## Limitations

- The dataset contains only 210 samples.
- The testing set contains only 32 samples.
- Only a Linear Kernel was evaluated.
- The same learning rate was used for all optimizers.
- The number of parameter updates differs between optimizers.
- The experiments are based on a single data split and random seed.

Therefore, the results demonstrate performance under the selected experimental conditions rather than the universal superiority of any optimization algorithm.
