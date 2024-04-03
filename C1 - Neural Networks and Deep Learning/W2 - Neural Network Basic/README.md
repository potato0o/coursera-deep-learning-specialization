# Week 2 - Neural Networks Basic

Progress: Done
Summary: Building simple neural network with logistic regression to understand the training process of forward propagation and backward propagation

[C1_W2.pdf](Week%202%20-%20Neural%20Networks%20Basic%200b010ce3e87240f189ffaf9dea5964dd/C1_W2.pdf)

# Week 2 - Neural Network Basic

## Standard Notation for Neural Network

General comments: 

- superscript $(i)$ will denote the $i^(th)$ training example while superscript $[l]$ will denote the $l^(th)$ layer

Sizes:

![Untitled](Week%202%20-%20Neural%20Networks%20Basic%200b010ce3e87240f189ffaf9dea5964dd/Untitled.png)

Objects:

![Untitled](Week%202%20-%20Neural%20Networks%20Basic%200b010ce3e87240f189ffaf9dea5964dd/Untitled%201.png)

![Untitled](Week%202%20-%20Neural%20Networks%20Basic%200b010ce3e87240f189ffaf9dea5964dd/Untitled%202.png)

Common forward propagation equation examples:

![Untitled](Week%202%20-%20Neural%20Networks%20Basic%200b010ce3e87240f189ffaf9dea5964dd/Untitled%203.png)

Examples of cost function:

![Untitled](Week%202%20-%20Neural%20Networks%20Basic%200b010ce3e87240f189ffaf9dea5964dd/Untitled%204.png)

## Deep Learning Representations

- nodes represent inputs, activations or outputs
- edges represent weights or biases

Here are several examples of Standard deep learning representations

![Untitled](Week%202%20-%20Neural%20Networks%20Basic%200b010ce3e87240f189ffaf9dea5964dd/Untitled%205.png)

![Untitled](Week%202%20-%20Neural%20Networks%20Basic%200b010ce3e87240f189ffaf9dea5964dd/Untitled%206.png)

## Binary Classification

In a binary classification problem, the result is a discrete value output. For example:

- account hacked(1) or not hacked(0)
- a tumor malign(1) or benign(0)

### Example: Cat vs Non-Cat

The goal is to train a classifier for which the input is an image represented by a feature vector, x, and predicts whether the corresponding labels is 1 or 0. In this case, whether this is a cat image(1) or non-cat image(0).

![Untitled](Week%202%20-%20Neural%20Networks%20Basic%200b010ce3e87240f189ffaf9dea5964dd/Untitled%207.png)

An image is stored in the computer in three separate matrices corresponding to the Red, Green, and Blue color channels of the image. The three matrices have the same size as the image, for example, the resolution of the cat image is 64 pixels X 64 pixels, the three matrices (RGB) are 64 X 64 each.

The value in a cell represents the pixel intensity which will be used to create a feature vector of n dimension. In pattern recognition and machine learning, a feature vector represents an image, Then the classifier's job is to determine whether it contain a picture of a cat or not.

To create a feature vector, 𝑥, the pixel intensity values will be “ unrolled” or “ reshaped” for each color. The dimension of the input feature vector𝑥 is 𝑛= 64𝑥 64𝑥 3 = 12288.

![Untitled](Week%202%20-%20Neural%20Networks%20Basic%200b010ce3e87240f189ffaf9dea5964dd/Untitled%208.png)

## Logistic Regression

Logistic regression is a learning algorithm used in a supervised learning problem when the output 𝑦 are all either zero or one. The goal of logistic regression is to minimize the error between its predictions and training data.

### Example Cat vs Non-cat

Given an image represented by a feature vector 𝑥, the algorithm will evaluate the probability of a cat being in that image.

[3. Logistic_Regression.pdf](Week%202%20-%20Neural%20Networks%20Basic%200b010ce3e87240f189ffaf9dea5964dd/3._Logistic_Regression.pdf)

## Logistic Regression (Cost Function)

[4. Logistic_Regression_Cost_Function.pdf](Week%202%20-%20Neural%20Networks%20Basic%200b010ce3e87240f189ffaf9dea5964dd/4._Logistic_Regression_Cost_Function.pdf)

## Forward and Backward Propagation for Logistic Regression (Simple NN)

Take logistic regression as simple neural network, in forward propagation, data X is feed into the model. A linear function (ax+b) is performed, where a and b are the weights of the data. After linear function, a sigmoid activation function is performed to determine the decision. Loss is calculate compared the training data. 

In back prop calculated loss is derivate for the calculation of gradient descent. The weights are updated using the derivative of loss. 

![Untitled](Week%202%20-%20Neural%20Networks%20Basic%200b010ce3e87240f189ffaf9dea5964dd/Untitled%209.png)