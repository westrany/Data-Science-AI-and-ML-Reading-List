# Data-Science-AI-and-ML-Reading-List
_My personal reading list with papers, books, articles and forum entries for Data Science, Machine Learning and Artificial Intelligence._  
_I've also included a brief summary of each paper for conveniency._  

## Index  

| Type       | Title         | Author | Year |
|------------|---------------|--------|------|
|Article |[A Neural Network in 13 lines of Python (Part 2 - Gradient Descent)](#a-neural-network-in-13-lines-of-python-part-2---gradient-descent) |Andrew Trask |2015 |
|Forum | [Common Cost Functions Used in Neural Networks](#common-cost-functions-used-in-neural-networks) |StackExchange Users |2015|
|Paper |[Deep Sparse Rectifier Neural Networks](#deep-sparse-rectifier-neural-networks) |Xavier Glorot, Antoine Bordes, and Yoshua Bengio |2011|
|Paper |[Efficient BackProp](#efficient-backprop) |Yann LeCun, Léon Bottou, Genevieve Orr, Klaus-Robert Müller |1998|  

## Articles

### [A Neural Network in 13 lines of Python (Part 2 - Gradient Descent)](https://iamtrask.github.io/2015/07/27/python-network-part2/)  
_Author: Andrew Trask_  
_Year: 2015_  

The article provides a hands-on guide to implementing backpropagation in Python for a simple neural network. It explains key steps in building the network, calculating gradients, and updating weights using Python code.  

**Key Contributions:**  

1. Feedforward Calculation: Demonstrates how to compute predictions from inputs using weights and activations.
2. Cost Function: Introduces quadratic cost (MSE) to evaluate network performance.
3. Backpropagation: Provides code to calculate errors, propagate them backward, and update weights accordingly.

**Impact:**  

This tutorial simplifies understanding of backpropagation, offering a practical starting point for beginners in neural network development.

---

## Forum  

### [Common Cost Functions Used in Neural Networks](https://stats.stackexchange.com/questions/154879/a-list-of-cost-functions-used-in-neural-networks-alongside-applications)  
_Authors: StackExchange Users_  
_Year: 2015_  

Cost functions are crucial in neural networks as they evaluate how well a network performs. These functions measure the difference between the predicted output and the actual output, guiding the network's learning process through backpropagation.  

**Key Cost Functions:**  

1. Quadractic Cost (Mean Squared Error)
    - This measures the squared difference between predicted and actual values. It is commonly used in regression tasks but can suffer from slow learning when errors are small.

2. Cross-Entropy Cost (Binary Cross-Entropy)
    - Widely used in classification tasks, this function performs better for models with probabilities as outputs.

3. Exponential Cost
    - This cost function amplifies larger errors, depending on the parameter 𝜏.
  
4. Hellinger Distance
    - This cost function ensures positive values and is ideal for distributions between 0 and 1.  

5. Kullback–Leibler Divergence (KL Divergence)  
    - Measures the information loss when using the network's output to approximate the target distribution.  

6. Generalized Kullback–Leibler Divergence
    - A variation of KL Divergence that adds an adjustment for the network's output.  

7. Itakura–Saito Distance
    - This function measures divergence, particularly useful in audio signal processing.
  
**Impact:**  

These cost functions play essential roles in training neural networks for various tasks, including regression, classification, and even specialized applications like audio processing. By selecting the right cost function, one can improve the network’s learning process and performance.

---

## Papers  

### [Deep Sparse Rectifier Neural Networks](https://proceedings.mlr.press/v15/glorot11a/glorot11a.pdf)
_Authors: Xavier Glorot, Antoine Bordes, and Yoshua Bengio_  
_Year: 2011_

The paper focuses on the use of the Rectified Linear Unit (ReLU) as an activation function in deep neural networks, which became highly influential in modern deep learning architectures.  

**Key Contributions:**  

1. Introduction of ReLU: The paper introduces and promotes the use of the Rectified Linear Unit (ReLU) activation function, which is defined as f(x)=max(0,x). This function addresses issues like vanishing gradients that occur with traditional sigmoid or hyperbolic tangent activation functions.

2. Sparse Activations: ReLU introduces sparsity in the neural network, meaning many neurons are inactive for a given input. This leads to better generalization and faster training times compared to traditional activation functions that produce dense activations.

3. Empirical Results: The paper provides experimental evidence showing that deep neural networks using ReLU activation outperform networks with sigmoid and tanh activations on various benchmarks. ReLU improves both the convergence speed and the final performance of deep networks.

4. Advantage in Training Deep Networks: By mitigating the vanishing gradient problem, ReLU allows for easier and more effective training of very deep networks. The authors also explore the behavior of ReLU compared to other nonlinearities in unsupervised pre-training scenarios.

**Impact:**  
This work was pivotal in making deep learning more feasible and widely adopted, especially in tasks involving deep convolutional networks. ReLU has since become the default activation function in many deep learning architectures.  

---

### [Efficient BackProp](https://yann.lecun.com/exdb/publis/pdf/lecun-98b.pdf)
_Authors: Yann LeCun, Léon Bottou, Genevieve Orr, and Klaus-Robert Müller_  
_Year: 1998_

The paper focuses on improving the efficiency of backpropagation, a fundamental algorithm for training neural networks, which is widely used in deep learning.

**Key Contributions:**  

1. Challenges with Basic BackProp: The paper identifies challenges like slow convergence, sensitivity to hyperparameters, and the vanishing/exploding gradient problem, which often affect deep networks using standard backpropagation.

2. Normalization: The authors highlight the importance of normalizing input data to improve training speed and performance by ensuring that all features are on comparable scales.

3. Weight Initialization: Careful weight initialization is recommended to avoid excessively small or large gradients, which can lead to poor training dynamics in deep networks.

4. Learning Rate Scheduling: The paper proposes dynamic adjustment of the learning rate during training to facilitate faster convergence and avoid overshooting the optimal solution.

5. Momentum: By incorporating momentum into gradient descent, the algorithm can escape local minima and reduce oscillations, leading to smoother and faster convergence.

6. Second-Order Methods: The paper explores second-order optimization techniques like Newton’s method, which consider the curvature of the loss surface, although these methods are computationally expensive.

**Impact:**  

This work was pivotal in optimizing the training process of neural networks and laid the foundation for modern training techniques, especially in deep learning applications. The recommendations made in this paper are still relevant and widely used in today’s machine learning models.


