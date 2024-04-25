# Optimization Algorithm

Progress: Not started

[C2_W2.pdf](Optimization%20Algorithm/C2_W2.pdf)

## Mini-batch Gradient Descent

Gradient descent can vary based on the number of training patterns used to calculate the error and update the model. There are three main variants:

1. **Batch Gradient Descent**: It uses the entire training dataset to compute the error and update the model. While it provides accurate gradients, it can be computationally expensive for large datasets.
2. **Stochastic Gradient Descent (SGD)**: In this method, only one training pattern is used at a time to calculate the error. It’s computationally efficient but can be noisy due to the randomness of individual samples.
3. **Mini-Batch Gradient Descent**: This approach strikes a balance by using a small batch of training patterns (mini-batch) to compute the error. It combines the advantages of both batch and stochastic gradient descent. Mini-batch sizes are typically chosen based on available memory and computational resources.

![Untitled](Optimization%20Algorithm/Untitled.png)

## Exponentially Weighted Average

1. **Exponentially Weighted Averages (EWMA):**
    - EWMA is a technique used to calculate a weighted average of a sequence of data points. It is commonly applied to smooth out noisy data, remove outliers, and identify trends or patterns over time.
    - In the context of time series analysis, EWMA is often used as a smoothing technique. [It adapts quickly to changes in data by giving more weight to recent observations while gradually decaying the influence of older observations1](https://medium.com/@dhartidhami/exponentially-weighted-averages-5de212b5be46)[2](https://shallbd.com/understanding-exponentially-weighted-moving-average-in-deep-learning/).
    - The formula for EWMA is as follows: $[ V_t = \beta \cdot V_{t-1} + (1 - \beta) \cdot \text{NewSample} ]$
        - $(V_t)$ represents the exponentially weighted average at time (t).
        - $(\beta)$ is a parameter (often between 0 and 1) that controls the weight given to recent data.
        - $(\text{NewSample})$ is the current data point.
    - By choosing an appropriate value for $(\beta)$, we control how much weight to give to the most recent data points when calculating the average. [Smaller (\beta) values result in slower adaptation to changes, while larger values give more weight to recent observations1](https://medium.com/@dhartidhami/exponentially-weighted-averages-5de212b5be46)[2](https://shallbd.com/understanding-exponentially-weighted-moving-average-in-deep-learning/).
    - EWMA is computationally efficient and memory-friendly, making it suitable for various applications, including machine learning optimizations.
2. **Machine Learning Applications:**
    - In machine learning, EWMA plays a role in optimization algorithms such as:
        - **Gradient Descent with Momentum:** EWMA helps smooth out gradients during optimization, leading to faster convergence and better performance.
        - **RMSprop:** EWMA is used to adjust the learning rate based on the moving average of squared gradients.
        - **[Adam (Adaptive Moment Estimation):** Adam combines EWMA of gradients and squared gradients to adaptively adjust learning rates3](https://medium.com/@tobias-chc/exponentially-weighted-average-5eed00181a09).
    - Using some form of exponentially weighted average can be beneficial over simple gradient descent, especially in neural networks where noisy gradients can impact training efficiency and stability.
    
    ![Untitled]([Optimization%20Algorithm/Untitled%201.png])
    
    1. **Bias Correction:**
    - To correct this bias, we can remove the effect of the initial guess (bias) from the moving average.
    - At each time step, we divide the current estimate by **1 - β**, where **β** is the smoothing factor (usually between 0 and 1).
    - The corrected estimate is given by: $[ \hat{A_t} = \frac{A_t - \beta A_{t-1}}{1 - \beta} ]$
    1. **Why Bias Correction Matters**:
        - Bias correction ensures that the initial estimate doesn’t unfairly influence the moving average.
        - Without bias correction, the estimate would be skewed towards the initial value, which may not reflect the true underlying trend.
        - By dividing by $(1 - \beta)$, we remove this bias and get a more accurate estimate.
    2. **Application in Deep Learning**:
        - In deep learning optimization algorithms like **Adam**, bias correction is crucial.
        - Adam includes bias corrections for both the first-order moments (momentum term) and second-order moments (uncentered variance) to account for their initialization at the origin.
        - These corrections help improve convergence during training.
    
    ## Gradient Descent with Momentum
    
    **Gradient Descent** is a popular optimization algorithm used to minimize the cost (loss) function during training. However, it has some limitations, including slow convergence and jittery paths. One of the issues is that it only considers the current gradient and learning rate, ignoring past steps taken in the cost space.
    
    **Momentum** is an enhancement to gradient descent that addresses these problems. Here’s how it works:
    
    1. **The Problem with Vanilla Gradient Descent**:
        - In vanilla gradient descent, weight updates depend solely on the current gradient and learning rate.
        - It can lead to slow convergence, especially around saddle points (where gradients are negligible or zero).
        - The path followed by gradient descent can be jittery, even with mini-batch updates.
    2. **How Momentum Fixes This**:
        - Imagine a ball rolling down a hill. As it gathers momentum, it can overcome plateaus and continue moving.
        - Similarly, we want to accumulate momentum during optimization to help navigate flat regions.
        - Momentum introduces a moving average of past gradients to guide weight updates.
    3. **Exponential Moving Average (EMA)**:
        - We compute the moving average of gradients using EMA.
        - EMA assigns greater weight to recent values and discounts older observations faster.
        - The EMA for a sequence of gradients is given by: $[ S(t) = \beta S(t-1) + (1 - \beta) \nabla J(w) ]$ where:
            - $(S(t))$ is the EMA at iteration $(t)$.
            - $(\beta)$ is the smoothing factor (between 0 and 1).
            - $(\nabla J(w))$ is the gradient at iteration $(t)$.
    4. **Weight Update with Momentum**:
        - The new weight update equation becomes: $[ w(t) = w(t-1) - \alpha S(t) ]$ where:
            - $(w(t))$ is the weight at iteration (t).
            - $(\alpha)$ is the learning rate.
    5. **Advantages of Momentum**:
        - Faster convergence: Momentum accelerates gradient vectors in the right direction.
        - Improved stability: It helps avoid getting stuck in local minima.
        - Overcoming plateaus: Gradients accumulated from past iterations push the cost further.
    
    ## RMSprop (Root Mean Square Propagation)
    
    **RMSprop (Root Mean Squared Propagation)**, an optimization algorithm commonly used in deep learning. RMSprop improves the convergence speed and stability of model training. Here’s how it works:
    
    1. **Motivation**:
        - RMSprop was first proposed by Geoffrey Hinton in lecture 6 of the online course “Neural Networks for Machine Learning.”
        - It falls into the category of **adaptive learning rate methods**.
        - Despite being unpublished, RMSprop is widely known and implemented in most deep learning frameworks.
    2. **Adaptation from Rprop**:
        - To understand RMSprop, let’s start with **rprop**, an algorithm used for full-batch optimization.
        - Rprop addresses the issue of varying gradient magnitudes. Gradients can be tiny or huge, making it challenging to find a single global learning rate.
        - In full-batch learning, using only the sign of the gradient ensures consistent weight updates.
        - However, we can’t increase learning rates arbitrarily because large gradients lead to divergence.
    3. **Individual Step Sizes**:
        - RMSprop combines the idea of using the sign of the gradient with individual step sizes for each weight.
        - Instead of looking at the gradient magnitude, we focus on the step size defined for each weight.
        - The step size adapts individually over time, allowing acceleration in the necessary direction.
    4. **RMSprop Algorithm**:
        - For weight (w), the step size adjustment is as follows:
            - Compute the moving average of squared gradients: $[ S(t) = \beta S(t-1) + (1 - \beta) \nabla J(w) ]$ where:
                - $(S(t))$ is the moving average at iteration (t).
                - $(\beta)$ is the smoothing factor (typically between 0 and 1).
                - $(\nabla J(w))$ is the gradient at iteration (t).
            - Update the weight: $[ w(t) = w(t-1) - \alpha \frac{\nabla J(w)}{\sqrt{S(t)}} ]$ where:
                - $(\alpha)$ is the learning rate.
    5. **Advantages of RMSprop**:
        - **Faster Convergence**: RMSprop adapts step sizes, leading to quicker convergence.
        - **Stability**: It helps avoid getting stuck in local minima.
        - **Handling Vanishing/Exploding Gradients**: Gradients in complex functions (like neural networks) tend to vanish or explode. RMSprop mitigates this issue.
        
        ## Difference of Momentum Gradient Descent and RMSProp
        
        Momentum Gradient Descent and RMSProp are both optimization algorithms used in machine learning, but they differ in how they update the weights during training:
        
        1. **Momentum Gradient Descent**: This algorithm introduces a moving average of past gradients to guide weight updates, hence the term 'momentum'. It accelerates gradient vectors in the right direction, leading to faster convergence. It also provides stability, helping to avoid getting stuck in local minima and overcoming plateaus. This is achieved by computing the moving average of gradients using an Exponential Moving Average (EMA), which assigns greater weight to recent values and discounts older observations faster.
        2. **RMSProp (Root Mean Square Propagation)**: RMSProp, on the other hand, adapts the learning rate individually for each weight, leading to quicker convergence. It also handles the issue of vanishing or exploding gradients, a common problem in complex functions like neural networks. The step size adapts individually over time, allowing acceleration in the necessary direction. This is achieved by computing the moving average of squared gradients, and using this to adjust the learning rate.
        
        ## Adam (Adaptive Moment Estimation)
        
        Adam is another popular optimization algorithm used in machine learning, and it combines the best properties of Momentum Gradient Descent and RMSProp.
        
        1. **Combining Momentum and RMSProp**: Adam uses the method of Momentum to use a moving average of past gradients, and the method of RMSProp to use a moving average of past squared gradients. This combination allows the algorithm to handle both the problems of Momentum and RMSProp effectively, leading to quicker convergence and more accurate training of the model.
        2. **Bias Correction**: Adam also includes a mechanism called bias correction to make the moving averages more reliable. This corrects the issue where the moving averages are initialized at zero and therefore are biased towards zero during early stages of training.
        3. **Algorithm**:
            - For each weight update, Adam calculates an exponentially decaying average of past gradients and an exponentially decaying average of past squared gradients.
            - Adam then uses these averages to adaptively change the learning rate for each weight in the model.
        4. **Advantages of Adam**:
            - **Efficiency**: Adam is computationally efficient and requires little memory.
            - **Adaptive Learning Rate**: Adam adapts the learning rate for each weight based on the moving averages of the gradients, allowing for a custom and more effective learning rate for each weight.
            - **Bias Correction**: The bias correction mechanism in Adam helps in providing a more accurate and reliable estimation of the moving averages.
            

## Learning Rate Decay

**Learning Rate Decay** is a technique used in machine learning models, particularly deep neural networks. It plays a crucial role in optimizing the training process. Let’s explore how it works:

1. **The Analogy**:
    - Imagine you’re searching for a coin you dropped in a large room. Initially, you take big steps, covering a lot of ground quickly.
    - As you get closer to the coin, you adjust your steps to be smaller and more precise.
    - Learning rate decay operates similarly: it starts with larger steps during training and gradually reduces them as the model converges.
2. **What Is the Learning Rate?**:
    - The **learning rate** determines how much the model adjusts its parameters (weights) based on the errors it makes during training.
    - If the learning rate is too high, the model might overshoot and miss the optimal solution.
    - If it’s too low, the model may converge too slowly or get stuck in local minima.
3. **The Purpose of Learning Rate Decay**:
    - Instead of keeping the learning rate constant throughout training, we gradually decrease it.
    - This gradual reduction ensures that the model starts with larger steps (high learning rate) when far from the optimal solution.
    - As training progresses, the learning rate decreases, allowing smaller, more precise adjustments.
4. **Methods for Learning Rate Decay**:
    - There are several techniques for reducing the learning rate:
        - **Step Decay**: Lower the learning rate at specific intervals (e.g., after a fixed number of training rounds).
        - **Exponential Decay**: Decrease the learning rate exponentially over time.
        - **(1/t) Decay**: Adjust the learning rate based on the iteration number.
    - The choice of method depends on the specific problem and model architecture.
5. **Benefits of Learning Rate Decay**:
    - **Faster Convergence**: Gradually reducing the learning rate helps the optimization algorithm converge more rapidly.
    - **Avoiding Oscillations**: Fixed learning rates can lead to oscillations or sluggish convergence. Decay mitigates these issues.
    - **Improved Model Performance**: Properly tuned learning rate decay can enhance training efficiency and overall model performance.
