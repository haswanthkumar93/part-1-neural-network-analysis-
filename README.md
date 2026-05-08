# Neural Network Analysis Project

## Project Overview

This project focuses on building and evaluating a feed-forward neural network using TensorFlow/Keras for customer churn prediction.

The project includes:
- Dataset understanding
- Data preprocessing
- Neural network model building
- Model training and evaluation
- Hyperparameter experimentation
- Final reflection and analysis

---

## Dataset Information

The dataset contains customer-related information used to predict whether a customer will churn or not.

The preprocessing steps included:
- Handling categorical variables
- Feature scaling
- Train-test splitting

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- TensorFlow / Keras

---

## Neural Network Architecture

The neural network models were built using:
- Dense layers
- ReLU activation function
- Sigmoid output layer
- Adam optimizer
- Binary crossentropy loss function

---

## Hyperparameter Experiments

Three different neural network configurations were tested by changing:
- Number of hidden layers
- Number of neurons
- Number of epochs
- Batch size

### Final Experiment Results

| Experiment | Hidden Layers | Neurons | Activation | Epochs | Batch Size | Accuracy |
|------------|---------------|----------|-------------|---------|-------------|-----------|
| Experiment 1 | 2 | 32 | ReLU | 25 | 32 | 0.9250 |
| Experiment 2 | 2 | 32 | ReLU | 30 | 32 | 0.9725 |
| Experiment 3 | 3 | 64 | ReLU | 50 | 16 | 0.9650 |

---

## Project Structure

```text
part-1-neural-network-analysis/
│
├── customer_churn_nn.csv
├── README.md
├── requirements.txt
├── notebook.ipynb
│
└── results/
    ├── evaluation_outputs.png
    ├── model_comparison_graph.png
    └── model_comparison_table.csv
```

---

## How to Run the Project

1. Install dependencies:

```bash
pip install -r requirements.txt
```

2. Open the notebook:

```text
notebook.ipynb
```

3. Run all cells from top to bottom.

---

## Conclusion

The experiments showed that deeper neural network architectures with additional epochs improved prediction accuracy. Hyperparameter tuning significantly enhanced the performance of the customer churn prediction model.