# Supervised Neural Networks

This repository contains implementations of three simple supervised neural networks using PyTorch, illustrating the use of residual connections, dense concatenations, and attention mechanisms in fully connected layers.

## Models

### 1. ResidualModel
- A feedforward network with a skip connection that concatenates the input to a latent layer output.
- Enables learning residual features to improve performance.

### 2. DenseNet
- Dense-style model concatenating inputs and latent representations at multiple stages.
- Promotes feature reuse and richer representations.

### 3. AttentionModel
- Incorporates attention weights on latent representations to emphasize important features.
- Uses softmax-based attention before passing through subsequent layers.

## Details
- Input layer takes 4-dimensional vectors.
- Hidden latent layers compress features to 2 or 3 dimensions.
- Output layer outputs 2-dimensional vectors with sigmoid activation.
- ReLU activation used in hidden layers.
- Softmax used for attention weight calculation in `AttentionModel`.

## Potential Improvements
- Add dropout/batch normalization to prevent overfitting.
- Replace soft attention with a true multi-head attention mechanism.
- Incorporate advanced loss functions (e.g., Focal Loss) for imbalanced data.