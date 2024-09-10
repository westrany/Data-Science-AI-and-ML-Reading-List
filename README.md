# Data-Science-AI-and-ML-Reading-List
_My personal reading list with papers, books and articles for Data Science, Machine Learning and Artificial Intelligence._  
_I've also included a brief summary of each paper for conveniency._  

## Index  

| Type       | Title         | Year |
|------------|---------------|------|
|Paper |[Deep Sparse Rectifier Neural Networks](#deep-sparse-rectifier-neural-networks) |2011|
|Paper |[Efficient BackProp](#efficient-backprop) | 1998|

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

The paper Efficient BackProp discusses various techniques to enhance the efficiency of backpropagation, a key algorithm for training neural networks.

**Key Concepts:**  

1. Backpropagation (BackProp)
Backpropagation is the most widely used method for training neural networks. It calculates the gradient of the loss function with respect to network weights by propagating the error backward from the output layer to the input layer.

2. Challenges with BackProp
Basic backpropagation can face issues like slow convergence, sensitivity to hyperparameters (e.g., learning rate), and difficulties with deep networks due to vanishing or exploding gradients.

3. Techniques for Efficient BackProp
The paper proposes several improvements to address these challenges:
    - Normalization: Input data should be normalized to ensure features are on similar scales, improving learning speed.
    - Weight Initialization: Initializing weights with small random values can prevent gradients from becoming too large or too small.
    - Learning Rate Scheduling: Dynamically adjusting the learning rate during training can help achieve faster convergence.
    - Momentum: Adding momentum to gradient descent helps escape local minima and speeds up convergence by reducing oscillations.

4. Second-Order Methods
Second-order optimization techniques (e.g., Newton’s method) approximate the curvature of the loss surface and improve convergence, although they are computationally expensive.

5. Activation Functions
Activation functions affect backpropagation efficiency. Sigmoid and hyperbolic tangent functions are prone to vanishing gradients. The paper suggests experimenting with alternative activation functions for better gradient flow.

6. Applications
The improvements discussed are applicable to various neural network architectures, such as Convolutional Neural Networks (CNNs), making backpropagation more powerful and efficient for complex models.


