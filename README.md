# Neural Network From Scratch

A from-scratch implementation of a neural network for MNIST handwritten digit classification, built entirely with NumPy without any deep learning frameworks.

## Purpose

This project demonstrates the fundamentals of neural networks by implementing core components manually, providing a hands-on learning experience for understanding how neural networks work under the hood.

## Tech Stack

- **Python 3**
- **NumPy** - Numerical computations and matrix operations
- **Pandas** - Data loading and preprocessing
- **Matplotlib** - Data visualization
- **Jupyter Notebook** - Interactive development environment

## Implementation Details

### Architecture

The neural network implements a simple 2-layer architecture:
- **Input Layer**: 784 neurons (28x28 flattened pixel values from MNIST images)
- **Hidden Layer**: 10 neurons with ReLU activation
- **Output Layer**: 10 neurons with Softmax activation (for digits 0-9)

### Core Components

| Component | Description |
|-----------|-------------|
| `init_params()` | Initializes weights and biases with random values |
| `ReLU()` | Rectified Linear Unit activation function |
| `softmax()` | Softmax activation for probability distribution output |
| `forward_prop()` | Forward propagation through the network |
| `one_hot()` | One-hot encoding for labels |
| `deriv_ReLU()` | Derivative of ReLU for backpropagation |
| `back_prop()` | Backpropagation to compute gradients |
| `update_params()` | Updates parameters using gradient descent |
| `gradient_descent()` | Training loop with accuracy tracking |

### Dataset

The project uses the MNIST dataset located in `data/`:
- `train.csv` - Training data with 785 columns (label +784 pixel values)
- `test.csv` - Test data for predictions
- `sample_submission.csv` - Sample submission format

## Installation

1. Clone the repository:
```bash
cd neural_network_from_scratch
```

2. Install required packages:
```bash
pip install numpy pandas matplotlib jupyter
```

## Usage

1. Launch Jupyter Notebook:
```bash
jupyter notebook notebook.ipynb
```

2. Run the cells sequentially to:
   - Load and preprocess the MNIST dataset
   - Initialize network parameters
   - Train the network using gradient descent
   - Evaluate accuracy on training and validation sets

## Project Structure

```
neural_network_from_scratch/
├── data/
│   ├── train.csv        # Training dataset
│   ├── test.csv         # Test dataset
│   └── sample_submission.csv
├── notebook.ipynb       # Main implementation notebook
└── README.md
```

## Learning Outcomes

This project helps understand:
- Matrix operations in neural networks
- Forward and backward propagation
- Activation functions and their derivatives
- Gradient descent optimization
- One-hot encoding for classification
- Softmax for multi-class classification