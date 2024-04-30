# Hyperparameter Tuning

Summary: hyperparameter tuning, batch norm and softmax activation
Progress: Done

[C2_W3.pdf](Hyperparameter%20Tuning/C2_W3.pdf)

## Tuning Process (Hierarchy)

In deep learning we have many hyperparameter to be considered and tuning for all these hyperparameters will be very complicated. Therefore a hierarchy of importance of the hyperparameters will help us ease the process of hyperparameter tuning.

1. Learning rate
2. mini-batch size
3. Number of hidden unit
4. Number of layer
5. Learning rate decay
6. Adam (Beta and Epsilon) - normally fixed to  the default value

## Batch Normalization (Batch Norm)

Batch normalization (Batch Norm) is a technique used in deep learning to improve the training of neural networks by normalizing the inputs of each layer. It was introduced to address the problem of internal covariate shift, where the distribution of inputs to each layer changes during training, leading to slower convergence and poor generalization.

Here's how batch normalization works:

1. **Normalization**: Batch Norm normalizes the activations of each layer by subtracting the batch mean and dividing by the batch standard deviation. This is similar to how data normalization is performed on the input data.
2. **Scaling and Shifting**: After normalization, the normalized activations are scaled and shifted using learnable parameters (gamma and beta). This allows the model to learn the optimal scale and shift for each activation.
3. **Mini-batch Statistics**: Instead of using the population mean and standard deviation, Batch Norm computes the mean and standard deviation of each feature dimension within a mini-batch during training. This introduces noise into the normalization process, which acts as a form of regularization and helps to stabilize training.
4. **Inference**: During inference, Batch Norm uses the moving average of mean and standard deviation computed during training to normalize the activations. This ensures that the model generalizes well to unseen data.

Batch normalization offers several benefits:

- **Improved Training Stability**: By normalizing the activations, Batch Norm reduces the internal covariate shift problem, leading to faster convergence and more stable training.
- **Regularization**: The noise introduced by batch-wise normalization acts as a form of regularization, reducing the need for other regularization techniques such as dropout.
- **Reduced Dependency on Initialization**: Batch Norm makes networks less sensitive to weight initialization, allowing for the use of higher learning rates and potentially speeding up training.

## Softmax Regression for Multi-class classification

Softmax regression, also known as **multinomial logistic regression**, is a popular technique used for **multi-class classification**. It’s an extension of the binary logistic regression model to handle more than two classes.

Here are the key points about softmax regression:

1. **Objective**:
    - Given an input feature vector (x), softmax regression assigns probabilities to each class label.
    - The goal is to predict the most likely class for a given input.
2. **Model Representation**:
    - Suppose we have (K) classes (e.g., different types of animals: cat, dog, bird).
    - For each class (k), we compute a score $(s_k(x))$ based on the input features $(x)$.
    - The scores are typically computed using a linear function: $(s_k(x) = w_k^T x + b_k)$, where $(w_k)$ is the weight vector and $(b_k)$ is the bias term for class $(k)$.
3. **Softmax Function**:
    - The softmax function converts raw scores into probabilities.
    - For class $(k)$, the probability is given by:  $[ P(y = k | x) = \frac{e{s_k(x)}}{\sum_{j=1}K e^{s_j(x)}} ]$
    - Here, (y) represents the true class label.
4. **Loss Function**:
    - We use the **cross-entropy loss** (also called the log loss) to train the model.
    - The loss for a single example is: $[ L(x, y) = -\log P(y | x) ]$
    - The overall loss over the entire dataset is the average of individual losses.
5. **Training**:
    - We optimize the model parameters (weights and biases) using gradient-based optimization methods (e.g., stochastic gradient descent).
    - The gradients are computed using backpropagation.
6. **Predictions**:
    - To make predictions, we choose the class with the highest probability: $[ \hat{y} = \arg\max_k P(y = k | x) ]$