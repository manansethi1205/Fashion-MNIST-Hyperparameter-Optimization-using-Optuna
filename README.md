# Fashion MNIST Hyperparameter Optimization using Optuna

An end-to-end Deep Learning project demonstrating automated hyperparameter optimization of a PyTorch neural network on the Fashion-MNIST dataset using **Optuna**.

Unlike manual trial-and-error tuning, this project uses Bayesian optimization to automatically search for high-performing neural network architectures and training configurations.

---

# Project Overview

Selecting the right neural network architecture and training hyperparameters is one of the most important aspects of building an effective deep learning model.

This project automates that process using **Optuna**, a hyperparameter optimization framework that efficiently explores the search space and identifies configurations that maximize validation accuracy.

The project builds upon a baseline Fashion-MNIST classifier and extends it by automatically tuning multiple architectural and optimization parameters.

---

# Dataset

Fashion-MNIST is a benchmark computer vision dataset consisting of **70,000 grayscale images** of clothing items across **10 categories**.

- Training Images: 60,000
- Test Images: 10,000
- Image Size: 28 × 28
- Classes: 10

Each image is flattened into a 784-dimensional feature vector before being passed to the neural network.

---

# Objective

The objective of this project is to maximize validation accuracy by automatically searching for the best neural network configuration instead of relying on manual experimentation.

---

# Technologies Used

- Python
- PyTorch
- Optuna
- NumPy
- Pandas
- Matplotlib
- Scikit-learn

---

# Neural Network Architecture

The model architecture is dynamically generated during each Optuna trial.

Each hidden layer consists of:

Linear Layer

↓

Batch Normalization

↓

ReLU Activation

↓

Dropout

↓

Output Layer

The number of hidden layers and neurons are selected automatically by Optuna during optimization.

---

# Hyperparameters Optimized

The following hyperparameters were searched automatically:

| Hyperparameter | Search Space |
|---------------|-------------|
| Hidden Layers | 1 – 5 |
| Neurons per Layer | 16 – 128 |
| Epochs | 40 – 110 |
| Learning Rate | 1e-5 – 1e-1 (Log Scale) |
| Dropout Rate | 0.1 – 0.5 |
| Batch Size | 16, 32, 64, 128 |
| Optimizer | SGD, Adam, RMSprop |
| Weight Decay | 1e-5 – 1e-3 |

---

# Optimization Strategy

Optuna creates multiple independent trials.

For each trial:

1. Sample a new set of hyperparameters.
2. Build a new neural network architecture.
3. Train the model.
4. Evaluate validation accuracy.
5. Record the performance.
6. Use previous trial results to guide future searches.

This iterative optimization process efficiently explores the hyperparameter space while minimizing unnecessary manual experimentation.

---

# Best Hyperparameters Found

After **25 optimization trials**, the following configuration achieved the highest validation accuracy:

| Hyperparameter | Best Value |
|---------------|-----------|
| Hidden Layers | 4 |
| Neurons per Layer | 128 |
| Epochs | 60 |
| Learning Rate | 0.01321 |
| Dropout Rate | 0.30 |
| Batch Size | 32 |
| Optimizer | Adam |
| Weight Decay | 9.32e-05 |

---

# Final Performance

Best Validation Accuracy

**89.38%**

The optimization process demonstrated how carefully selecting training hyperparameters can significantly improve model performance over manually chosen configurations.

---

# Project Workflow

Fashion-MNIST Dataset

↓

Data Preprocessing

↓

Train / Validation Split

↓

Optuna Trial

↓

Generate Hyperparameters

↓

Build Neural Network

↓

Train Model

↓

Evaluate Validation Accuracy

↓

Store Trial Results

↓

Repeat for Multiple Trials

↓

Select Best Model

---

# Key Concepts Demonstrated

- Artificial Neural Networks
- PyTorch Model Building
- Dynamic Neural Network Construction
- Batch Normalization
- Dropout Regularization
- Hyperparameter Optimization
- Bayesian Optimization
- Neural Architecture Search
- Learning Rate Optimization
- Optimizer Comparison
- Weight Decay Regularization
- Model Selection
- Deep Learning Experimentation

---

# What I Learned

Through this project I gained practical experience in:

- Designing configurable neural network architectures.
- Using Optuna for automated hyperparameter optimization.
- Understanding the impact of learning rate on convergence.
- Comparing optimizers such as SGD, Adam and RMSprop.
- Exploring how network depth affects model performance.
- Investigating the effect of dropout and weight decay on generalization.
- Building reproducible deep learning experimentation pipelines.
- Evaluating multiple candidate models to identify the best performing configuration.

---

# Improvements over the Baseline Model

Compared to my previous Fashion-MNIST implementation, this project introduces:

- Automated hyperparameter optimization using Optuna.
- Dynamic neural network generation.
- Automated optimizer selection.
- Learning rate optimization.
- Batch size optimization.
- Weight decay tuning.
- Dropout optimization.
- Neural architecture search.
- Multiple trial-based model evaluation.
- Reproducible experimentation workflow.

---

# Future Improvements

- CNN-based Hyperparameter Optimization
- Early Stopping
- Learning Rate Scheduling
- Optuna Pruning
- TensorBoard Integration
- K-Fold Cross Validation
- Mixed Precision Training
- Transfer Learning Experiments

---

# Repository Structure

```
Fashion-MNIST-Hyperparameter-Optimization-using-Optuna/
│
├── notebook/
│   └── Fashion_MNIST_Hyperparameter_Optimization.ipynb
├── README.md
├── requirements.txt
```

---

# Skills Demonstrated

- Python
- PyTorch
- Optuna
- Deep Learning
- Neural Networks
- Hyperparameter Optimization
- Bayesian Optimization
- Model Selection
- Machine Learning
- Data Preprocessing
- GPU Training
- Experiment Tracking

---

# Author

**Manan Sethi**
Aspiring AI/ML Engineer with interests in Deep Learning, Computer Vision, Machine Learning and Data Science.
