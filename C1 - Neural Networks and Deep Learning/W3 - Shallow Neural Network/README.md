# Week 3 - Shallow Neural Network

Progress: Done
Summary: Building of shallow NN with multiple hidden layer nodes. Intro to activation function

[C1_W3.pdf](Week%203%20-%20Shallow%20Neural%20Network%20b8190887359641c88221b08239824dc9/C1_W3.pdf)

# Shallow Neural Network

## Recap on Single Node Hidden Layer NN

![Untitled](Week%203%20-%20Shallow%20Neural%20Network%20b8190887359641c88221b08239824dc9/Untitled.png)

In single hidden unit NN, we only compute one time of forward and backward propagation. The hidden unit consist of one node only. In this week, we will implement a shallow NN with 1 hidden unit and multiple nodes on hidden unit.

## Single Hidden Layer with Multiple Nodes

![Untitled](Week%203%20-%20Shallow%20Neural%20Network%20b8190887359641c88221b08239824dc9/Untitled%201.png)

As shown in the figure above, the NN may contain multiply hidden layer nodes, and each of the node receive input from X and perform a liner regression. The mathematical formulation of NN with multiple node hidden layer is:

![Untitled](Week%203%20-%20Shallow%20Neural%20Network%20b8190887359641c88221b08239824dc9/Untitled%202.png)

![Untitled](Week%203%20-%20Shallow%20Neural%20Network%20b8190887359641c88221b08239824dc9/Untitled%203.png)

Parameter involved in the NN above is: $W1 , b1, W2, b2$ ; where size of them is:

W1 = [number of hidden layer node, number of input features xn]

b1 = [number of hidden layer node, 1]

W2 = [number of output Y, number of hidden layer node]

b2 = [number of output Y, 1]

### Forward Propagation

![Untitled](Week%203%20-%20Shallow%20Neural%20Network%20b8190887359641c88221b08239824dc9/Untitled%204.png)

### Gradient Descent

Gradient calculation:

![Untitled](Week%203%20-%20Shallow%20Neural%20Network%20b8190887359641c88221b08239824dc9/Untitled%205.png)

## Activation Function

In previous model, we only use sigmoid as our activation function, but there are more optimized and suitable activation function for example **sigmoid**, **tanh**, and **ReLU (Rectified Linear Unit)** activation functions in the context of neural networks:

1. **Sigmoid Activation Function**:
    - **Formula**:
        
        $\sigma(x) = \frac{1}{1 + e^{-x}}$
        
    - **Range**: Outputs values between 0 and 1.
    - **Properties**:
        - Non-linear: Introduces non-linearity, allowing neural networks to capture complex patterns.
        - Interpretation: Often used for binary classification (e.g., probability of an event).
        - Symmetry: Not centered around zero.
        - Sensitivity: For inputs close to zero, small changes lead to large output changes.
    - **Advantage**: Smooth gradient, suitable for backpropagation.
    - **Limitation**: Prone to vanishing gradients for very large or small inputs.
2. **Tanh (Hyperbolic Tangent) Activation Function**:
    - **Formula**:
        
        $\tanh(x) = 2 \cdot \sigma(2x) - 1$
        
    - **Range**: Outputs values between -1 and 1 (centered around zero).
    - **Properties**:
        - Non-linear: Similar to sigmoid but centered at zero.
        - Symmetry: Output is symmetric around zero.
        - Sensitivity: Moderate gradient for inputs near zero.
    - **Advantage**: Captures both positive and negative values.
    - **Use Case**: Hidden layers in neural networks.
3. **ReLU (Rectified Linear Unit) Activation Function**:
    - **Formula**:
        
        $\text{ReLU}(x) = \max(0, x)$
        
    - **Range**: Outputs zero for negative inputs, otherwise linear.
    - **Properties**:
        - Non-linear: Simple and computationally efficient.
        - Sparsity: Encourages sparsity by zeroing out negative activations.
        - Gradient: Easy to compute (no exponent), faster convergence.
    - **Advantage**: Solves vanishing gradient problem, widely used in deep networks.
    - **Limitation**: “Dying ReLU” issue (some neurons remain inactive).
4. **Comparison**:
    - **Computational Simplicity**:
        - ReLU: Simple “if” statement, efficient.
        - Sigmoid: Requires computing an exponent.
    - **Output Range**:
        - Tanh > Sigmoid > ReLU (in terms of range).
    - **Training Efficiency**:
        - ReLU converges faster than sigmoid and tanh.
        - Sigmoid and tanh can be slower due to exponent calculations.

In summary, choose the activation function based on your specific problem, network architecture, and training requirements. ReLU is commonly preferred for hidden layers due to its simplicity and faster convergence, while sigmoid and tanh have their own use cases. 🚀🧠

![Untitled](Week%203%20-%20Shallow%20Neural%20Network%20b8190887359641c88221b08239824dc9/Untitled%206.png)