# Data-Science-AI-and-ML-Reading-List
_My personal reading list with papers, books and articles for Data Science, Machine Learning and Artificial Intelligence._  
_I've also included a brief summary of each paper for conveniency._

## Papers  
### [Efficient BackProp (1998)](https://yann.lecun.com/exdb/publis/pdf/lecun-98b.pdf)
_Authors: Yann LeCun, Léon Bottou, Genevieve Orr, and Klaus-Robert Müller_

The paper Efficient BackProp discusses various techniques to enhance the efficiency of backpropagation, a key algorithm for training neural networks.

Key Concepts
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

