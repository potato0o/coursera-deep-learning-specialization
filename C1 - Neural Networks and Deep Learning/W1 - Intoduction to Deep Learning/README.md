# Week 1 Introduction to Deep Learning

Progress: Done
Summary: Introduction to Neural Network and Supervised Learning

<a href="https://github.com/potato0o/coursera-deep-learning-specialization/blob/f69c77040c5f20d0ef9c97519f416046b3f7e595/C1%20-%20Neural%20Networks%20and%20Deep%20Learning/W1%20-%20Intoduction%20to%20Deep%20Learning/Week%201%20Introduction%20to%20Deep%20Learning/C1_W1.pdf">C1-W1 Notes<a>

## 5 Courses in Specialization

1. Neural Networks and Deep Learning (this course)
2. Improving deep Neural Networks: Hyperparameter tuning, regularization and Optimization
3. Structuring your Machine Learning Project
4. Convolutional Neural Networks
5. Natural Language Processing: Building sequence models

## Outline of this course

1. Introduction
2. Basics of Neural Network Programming
3. One Hidden Layer Neural Networks
4. Deep Neural Networks

# Week 1: Introduction

## What is Neural Network?

A **neural network** is a machine learning model that imitates the way the human brain makes decisions. It achieves this by using processes that mimic the behavior of biological neurons. Let’s break down the key components of a neural network:

1. **Nodes (Artificial Neurons)**: A neural network consists of interconnected nodes, also known as artificial neurons. These nodes are organized into layers:
    - **Input Layer**: The initial layer that receives input data.
    - **Hidden Layers**: One or more intermediate layers between the input and output layers.
    - **Output Layer**: The final layer that produces the network’s output.
    
    ![alt text](https://github.com/potato0o/coursera-deep-learning-specialization/blob/f69c77040c5f20d0ef9c97519f416046b3f7e595/C1%20-%20Neural%20Networks%20and%20Deep%20Learning/W1%20-%20Intoduction%20to%20Deep%20Learning/Week%201%20Introduction%20to%20Deep%20Learning/Untitled.png?raw=true)


1. **Weights and Thresholds**:
    - Each node has its own associated weight and threshold.
    - Weights determine the importance of input variables, with larger weights contributing more significantly to the output.
    - Thresholds define the activation condition for a node.

       ![alt text](https://github.com/potato0o/coursera-deep-learning-specialization/blob/f69c77040c5f20d0ef9c97519f416046b3f7e595/C1%20-%20Neural%20Networks%20and%20Deep%20Learning/W1%20-%20Intoduction%20to%20Deep%20Learning/Week%201%20Introduction%20to%20Deep%20Learning/Untitled%201.png?raw=true)
    

1. **Activation Function**:
    - After multiplying inputs by their respective weights and summing them, the output passes through an activation function.
    - If the output exceeds a specified threshold, the node activates and passes data to the next layer.
    - This process defines the neural network as a **feedforward network**.

## Supervised Learning

- Supervised learning, also known as **supervised machine learning**, involves using **labeled data sets** to train algorithms.
- The goal is to **classify data** or **predict outcomes** accurately based on input features and their corresponding labels.
- The data need to provide both the input and output for the machine to learn and predict the output accodingly.

![alt text](https://github.com/potato0o/coursera-deep-learning-specialization/blob/f69c77040c5f20d0ef9c97519f416046b3f7e595/C1%20-%20Neural%20Networks%20and%20Deep%20Learning/W1%20-%20Intoduction%20to%20Deep%20Learning/Week%201%20Introduction%20to%20Deep%20Learning/Untitled%202.png?raw=true)


- **Structured Data**: Structured data refers to organized information that follows a predefined format and resides in fixed fields within a record or file.
- **Unstructured Data:** Unstructured data lacks a specific structure and doesn’t neatly fit into databases.

    ![alt text](https://github.com/potato0o/coursera-deep-learning-specialization/blob/f69c77040c5f20d0ef9c97519f416046b3f7e595/C1%20-%20Neural%20Networks%20and%20Deep%20Learning/W1%20-%20Intoduction%20to%20Deep%20Learning/Week%201%20Introduction%20to%20Deep%20Learning/Untitled%203.png?raw=true)
    
    

## Why is Deep Learning taking off?

![alt text](https://github.com/potato0o/coursera-deep-learning-specialization/blob/f69c77040c5f20d0ef9c97519f416046b3f7e595/C1%20-%20Neural%20Networks%20and%20Deep%20Learning/W1%20-%20Intoduction%20to%20Deep%20Learning/Week%201%20Introduction%20to%20Deep%20Learning/Untitled%204.png?raw=true)

- In traditional machine learning algorithm, its found that when the size of training data reached certain size, the performance of the model would not increase.
- In Neural Network, the larger NN will increase in performance when data size increase. Therefore larger NN had been used as data size had surged as a result from digitalize.

![alt text](https://github.com/potato0o/coursera-deep-learning-specialization/blob/f69c77040c5f20d0ef9c97519f416046b3f7e595/C1%20-%20Neural%20Networks%20and%20Deep%20Learning/W1%20-%20Intoduction%20to%20Deep%20Learning/Week%201%20Introduction%20to%20Deep%20Learning/Untitled%205.png?raw=true)

- The significant improvement in data, computation and algorithms has dramatically boosted the development and employment of deep learning.
