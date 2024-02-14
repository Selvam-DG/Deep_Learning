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
  - 
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





