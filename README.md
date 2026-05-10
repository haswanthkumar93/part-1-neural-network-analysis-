# Part 1: Neural Network Fundamentals and Training Behavior Analysis

## Project Overview

This project focuses on building and analyzing a Feed-Forward Neural Network (FNN) for a supervised learning problem using a structured customer churn dataset.

The main objective of this project is to understand how neural networks learn through:
- Forward propagation
- Loss calculation
- Backpropagation
- Weight and bias updates
- Hyperparameter tuning

The model predicts whether a customer is likely to churn or remain with the company.

# Dataset Information

## Dataset Name
`customer_churn_nn.csv`

## Problem Type
Binary Classification

## Target Variable
`churn`

- `1` → Customer churned
- `0` → Customer retained

# Feature Description

## Numerical Features
- tenure_months
- monthly_charges
- total_charges
- avg_data_usage_gb
- support_tickets
- late_payments
- satisfaction_score
- discount_usage
- referral_count

## Categorical Features
- region
- plan_type
- contract_type
- payment_method

## Ignored Column
- customer_id (used only as an identifier)

# Task 1: Dataset Understanding

The dataset was explored to understand:
- Number of rows and columns
- Data types of features
- Distribution of the target variable
- Missing values
- Statistical summary of numerical features

### Observations
- The dataset contains both numerical and categorical features.
- The target variable is binary.
- Some features required encoding and scaling before training.

# Task 2: Data Preprocessing

Several preprocessing steps were applied before training the neural network.

## Preprocessing Steps

### Handling Missing Values
The dataset was checked for null values and cleaned if necessary.

### Encoding Categorical Variables
Categorical columns were converted into numerical form using encoding techniques.

### Feature Scaling
Numerical features were normalized to improve neural network performance.

### Train-Test Split
The dataset was divided into:
- 80% Training Data
- 20% Testing Data

# Task 3: Neural Network Model Building

A Feed-Forward Neural Network was built using TensorFlow/Keras.

## Model Architecture

### Input Layer
Receives the processed input features.

### Hidden Layer
- Dense neural network layer
- Activation function used: ReLU

### Output Layer
- Single neuron
- Sigmoid activation function for binary classification

# Loss Function

Binary Crossentropy was used because the problem is binary classification.

# Optimizer

Adam optimizer was selected for efficient training and faster convergence.

# Task 4: Training and Evaluation

The model was trained using the training dataset and evaluated on the testing dataset.

## Evaluation Metrics Used
- Training Accuracy
- Training Loss
- Testing Accuracy
- Testing Loss
- Confusion Matrix
- Classification Report

# Results and Interpretation

## Training Performance
The neural network successfully learned patterns from the training data and reduced loss over epochs.

## Testing Performance
The model achieved good prediction performance on unseen test data.

## Confusion Matrix Analysis
The confusion matrix helped evaluate:
- True Positives
- True Negatives
- False Positives
- False Negatives

This provided better insight into prediction quality beyond simple accuracy.

# Task 5: Hyperparameter Experimentation

Different hyperparameters were tested to observe their impact on model performance.

| Experiment | Hidden Layers | Neurons | Learning Rate | Batch Size | Epochs | Activation Function | Performance |
|------------|---------------|----------|----------------|------------|--------|---------------------|-------------|
| Experiment 1 | 1 | 32 | 0.001 | 32 | 20 | ReLU | Good |
| Experiment 2 | 2 | 64 | 0.001 | 16 | 30 | ReLU | Better |
| Experiment 3 | 1 | 128 | 0.01 | 32 | 40 | Tanh | Moderate |

# Hyperparameter Analysis

## Hidden Layers
Increasing hidden layers improved learning capability but excessive layers may increase overfitting risk.

## Number of Neurons
More neurons improved representation power but also increased computational complexity.

## Learning Rate
- High learning rate caused unstable learning.
- Low learning rate slowed down convergence.

## Batch Size
Smaller batch sizes improved stability while larger batch sizes reduced training time.

## Epochs
More epochs improved learning initially, but too many epochs could lead to overfitting.

# Task 6: Final Reflection

## Role of Weights and Biases

### Weights
Weights determine the importance of each input feature during prediction.

### Biases
Biases help shift activation outputs and improve the flexibility of the model.

Both are updated during backpropagation to reduce prediction error.

# Why Activation Functions Are Required

Activation functions introduce non-linearity into the network.

Without activation functions:
- The neural network behaves like a linear model.
- Complex relationships in data cannot be learned effectively.

ReLU activation helps the model learn complex patterns efficiently.

# Effect of Learning Rate

## Very High Learning Rate
- Training becomes unstable.
- Loss may fluctuate or diverge.

## Very Low Learning Rate
- Training becomes extremely slow.
- Model may take longer to converge.

Selecting an appropriate learning rate is important for stable learning.

# Underfitting and Overfitting

## Underfitting
Occurs when the model is too simple and fails to learn meaningful patterns.

### Signs
- Low training accuracy
- Low testing accuracy

## Overfitting
Occurs when the model memorizes training data and performs poorly on new data.

### Signs
- Very high training accuracy
- Lower testing accuracy
The final model showed balanced performance with minimal overfitting.

# Libraries Used
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- TensorFlow
- Keras

# Conclusion

This project demonstrated the complete workflow of building and analyzing a neural network for a binary classification problem.

The project covered:
- Data preprocessing
- Neural network architecture
- Model training
- Performance evaluation
- Hyperparameter experimentation
- Neural network learning behavior analysis

The experiments helped understand how neural networks learn and how different hyperparameters affect model performance.