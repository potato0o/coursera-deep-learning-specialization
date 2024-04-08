# Week 4 - Deep Neural Network

Progress: Done
Summary: Guidance to build deep neural network which consist of multiple layer of hidden unit and multiple node

[C1_W4.pdf](Week%204%20-%20Deep%20Neural%20Network%20b449043848c54c6a861fffe9edc2f0d3/C1_W4.pdf)

# Deep Neural Network

A **deep neural network (DNN)** is a powerful architecture that has revolutionized the field of artificial intelligence. Let’s delve into what it is and why it’s so significant:

## **What Are Deep Neural Networks?**

- A **deep neural network** (DNN) is an extension of the traditional artificial neural network (ANN).
- While ANNs have a simple structure with an input layer, one or two hidden layers, and an output layer, DNNs go deeper.
- DNNs consist of multiple layers, each adding complexity to the model. These layers include:
    - **Convolutional layers**: Ideal for image processing tasks.
    - **Max-pooling layers**: Used for down-sampling and feature extraction.
    - **Dense layers**: Handle complex relationships in the data.
    - And other unique layers tailored to specific problems.
- The additional depth allows DNNs to tackle intricate challenges like computer vision, natural language processing, and more.

![Untitled](Week%204%20-%20Deep%20Neural%20Network%20b449043848c54c6a861fffe9edc2f0d3/Untitled.png)

## Matrix Dimension of Parameters

Having a correct dimension of parameters is important to avoid and error during coding, below is the matrix dimension:

- $W^{[l]} = ( n^{[l]}, n^{[l-1]})$
- $b^{[l]} = ( n^{[l]}, 1)$
- $dW^{[l]} = ( n^{[l]}, n^{[l-1]})$
- $db^{[l]} = ( n^{[l]}, 1)$

where;

  $l = l^{th}$ layer of hidden layer

$n =$  number of node 

$n^{[l]} =$ number of node of $l^{th}$ layer of hidden layer

$n^{[l-1]} =$ number of nodes of $l^{th}-1$ layer of hidden layer

## Forward propagation of deep NN

![Untitled](Week%204%20-%20Deep%20Neural%20Network%20b449043848c54c6a861fffe9edc2f0d3/Untitled%201.png)

[Feedforward Neural Networks in Depth, Part 1: Forward and Backward Propagations](https://jonaslalin.com/2021/12/10/feedforward-neural-networks-part-1/)

[Feedforward Neural Networks in Depth, Part 2: Activation Functions](https://jonaslalin.com/2021/12/21/feedforward-neural-networks-part-2/)

[Feedforward Neural Networks in Depth, Part 3: Cost Functions](https://jonaslalin.com/2021/12/22/feedforward-neural-networks-part-3/)