# Deep_Learning
### Why?
- Big Data, GPU, and better algorithms and techniques
- TensorFlow and PyTorch are Deep Learning frameworks/ libraries

### Human Neuron –Signaling Mechanism
1. Excitatory stimuli reach the neuron
   - Input
2. Threshold is reached
3. Neuron fires and triggers an action potential
   - Output
     
### The Perceptron
- The structural building block of deep learning
- Forward Propagation
  - output = nonlinear activation function *( bias +  Σ summation og all (weight*inputs))
  - y = sigma * summation( Wi*xi +b)
- Loss Function: Comparision metric between predicted output  and actual output
  - cross-entropy loss: (-y * log(µ(x,w))) - ((1-y) * log(1-µ(x,w)))
- activation Function (Threshold) :
  1. Sigmoid
     - σ(x) = 1 / (1 + exp(-x))
  2. Hyperbolic Tangent
     - σ(x) = tanh(x)
  3. ReLU - Rectified Linear Unit
     - σ(x) = max(x,0)    
- The purpose of activation functions is to introduce non-linearities to the network

![Screenshot 2024-02-14 175705](https://github.com/Selvam-DG/Deep_Learning/assets/98681717/68664083-00c7-4ec1-8cb9-18f7485eaca9)

### Multilayer Perceptron
- A multilayer perceptron is a neural network with multiple perceptrons
- It is oftentimes organized into layers
- Each layer has its own set of parameters (weights 𝑾𝑖 and bias 𝒃𝑖)
- The underlying computation is a matrix multiplication described by 𝒚𝑖+1 = 𝜎(𝑾𝑖 ⋅𝒚𝑖 +𝒃𝑖)


![Screenshot 2024-02-14 175757](https://github.com/Selvam-DG/Deep_Learning/assets/98681717/cf69a10c-8bba-4d8e-8abc-af76484a4a61)

- z = 𝜎(𝑾1⋅𝒙+𝒃1)
- y = 𝜎(𝑾2⋅z+𝒃2)
- Y = 𝜎(𝑾2⋅(𝜎 𝑾1⋅𝒙+𝒃1) +𝒃2)

  
- Dense layer:
  - All inputs are densely connected to all outputs, these layers are known as dense layer
#### The Loss Function
 - We need a comparison metric between the predicted outputs 𝒚𝑖 and the expected outputs 𝒚𝑖
 - This is called the loss function, which usually depends on the type of problem the multilayer perceptron solves
   - For regression, a common metric is the mean squared error
   - For classification, a common metric is the cross-entropy
- Quantifying loss:
  - The loss of our network measures the cost incurred from incorrect predictions
  - L(f(x;W),y) i.e, L(predicted value, actual value)
- Empirical Loss
  - It measures the total loss over our entire dataset
  - an average of all loss
  - J(W) = (1/n) *  ΣL(f(x;W),y)
- Binary cross-entropy loss
  - cross-entropy loss can be used with models whose output probabilities are between 0 and 1
  - J(W) = cross-entropy loss: (Σ(-y^i * log(f(x^i,W))) - ((1-y^i) * log(1-f(x^i,W))) ) / n
- Mean Squared Error Loss
  - sum of the square of the difference between actual and predicted  output values
  - J(W) = (1/n) * Σ( y^i - f(x^i,W) )^2 


#### Cross Entropy – Class Probability and Softmax
- For classification, each output 𝑦1,…,𝑦𝑛 represents a class energy
- If the target class index is 𝑖, then only 𝑦𝑖 = 1 and all other 𝑦𝑗 = 0,𝑖 ≠ 𝑗 (this is also called one-hot encoding)
  - Example for class 1: 𝑦 = (1 0 0 0 0)'
  - Example for class 3: 𝑦 = ( 0 0 1 0 0)'
- To ensure that we have probabilities, we apply a softmax transformation
  -  𝑦𝑖 =exp(𝑦𝑖) / Σexp(𝑦𝑗)

- General weaknesses of Gradient Descend
  - Multiple local minima are common
  - Into which the network converges to depends heavily on random initialization
  - Success depends on learning rate


- How wrong is the current set of parameters 𝜽? Forward Propagation
  - In the forward prop, the output of the previous layer is updated to the current layer
- How should we change the set of parameters by ∇𝜽? Backward Propagation
  - In backward propagation, the weights are updated to the previous layer

### Loss Optimization
- we want to find the network weight that achieves the  lowest loss
- **W*** = argmin J(W) = argmin (1/n) *  ΣL(f(x^i;W),y^i)

### Parameter Optimization
- At this stage, we can compute the gradient of the parameters ∇𝜽
- The gradient tells us how we need to change the current parameters 𝜽 in order to make fewer errors on the given data
- We can use this in an iterative algorithm called gradient descent, with the central equation being 𝜽^i+1 = 𝜽^𝑖 −𝜇⋅∇𝜽^𝑖
- The learning rate 𝜇 tells us how quickly we should change the current parameters 𝜽^i
 - limitations:
   - The learning rate 𝜇 can lead to slow convergence if not properly configured
   - Large learning rates result in overshoot, become unstable, and diverge
   - Slow learning rates converge slowly and get stuck to false local minima
   - Stable learning rates converge smoothly and avoid local minima
  - Adaptive learning rates are good

- Gradient Descent
  - Gradient Descent incrementally adjusts the parameters 𝜽 based on the gradient ∇𝜽 of the parameters
     - For each iteration
       1. Compute the error of the parameters 𝜽
       2. Compute the gradient of the parameters ∇𝜽
       3. Update parameters using 𝜽^𝑖+1 = 𝜽^𝑖 − 𝜇 ⋅ ∇𝜽^i
 - There is no guarantee that the algorithm converges to the global optimum (e.g., due to learning rate 𝜇 or initial parameters 𝜽^1)
###ä Gradient Descent Algorithm
- SGD ( Stochastic Gradient Descent)
- Adam
- Adadelta
- Adagrad
- RMSProp
- **Stochastic Gradient Descent**
   - Algorithm
     - Initialize weights randomly
     - Loop until convergence
     -    pick a single data point i
     -    compute gradients
     -    update weights
     - Return weights


### How do our models learn?
- We thus need to loop over the training data 𝒙1, 𝒚1,…,𝒙𝑛,𝒚𝑛) to compute sums over individual data points 
- This results in a slight modification to the gradient descent algorithm
 1. For each epoch – Loop over training data
   2. For each batch – Loop over pieces of training data
     3. Compute the error of the parameters 𝜽
     4. Compute the gradient of the parameters ∇𝜽
     5. update parameters using 𝜽^𝑖+1 = 𝜽^𝑖 − 𝜇 ⋅ ∇𝜽^i

- **The Concept of Epochs**
  - Gradient descent requires multiple iterations to reach a minimum
  - The optimization function 𝑓(𝜽) individual data point sums the loss functions 𝐿(𝒚^𝑖,𝒚𝑖) of each (x𝑖, 𝒚𝑖) in the training data
  - We need to go through the training data multiple times to find suitable parameters 𝜽 for our problem
  - Each such iteration is called an epoch
  - Requires the computation of the full sum, which is expensive
 
- **The Concept of Batches**:
  - Instead of computing the full sum of one epoch in one go, we instead break it apart into multiple smaller pieces
  - These pieces are usually of a specified size (e.g., 64), which tells us how many training data points to use for each piece
  - One epoch then consists of processing all the pieces
  - Each such piece of the training data is called a batch

- **The Learning Process – A Summary**
  - The parameters 𝜽 are optimized by iterating through the training data
  - For practical reasons, this is split into epochs and batches

### The problem of Overfitting
#### Regularization:
- It is a Technique that constrains our optimization problem to discourage complex models
- We need this technique to improve the generalization of our model on unseen data
- There are two regularizations to avoid overfitting
  1. Regularization 1- Dropout
     - During training, randomly set some activations to 0
  2. Regularization 2- Early stopping
     - Stop training before we have a chance to overfit







sources: FAU University, learnbay, google, MIT_DeepLearning 





