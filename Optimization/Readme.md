## Optimization in DL:
#### What is optimization?
- Search of Local minima
- Search for better results
- Search for some convenient
- Search for best hypothesis
- Search for best mode

### SGT (Stochastic Gradient Descent)
  - In stochastic gradient descent, instead of taking a step by computing the gradient of the loss function creating by umming all the loss functions, we take a step by computing the gradient of the loss of only one randomly sampled (without replacement) example
  - Momentum
    - Better known as SGD with Momentum
### Adagrad (Adaptive Gradient)
  - Adapts the learning rate based on parameters
  - Performing smaller updates(i.e. low learning rates) for parameters associated with frequently occurring features, and larger updates (i.e. high learning rates) for parameters associated with infrequent features. For this reason, it is well-suited for dealing with sparse data
### Adadelta
  - Adadelta is an extension of Adagrad that seeks to reduce its aggressive, monotonically decreasing learning rate. Instead of accumulating all past squared gradients, Adadelta restricts the window of accumulated past gradients to some fixed size w
### RMSProp
  - The only difference RMSProp has with Adagrad is that the gt term is calculated by exponentially decaying average and not the sum of gradients
### Adam (Adaptive Moment Estimation)
  -  It uses both first order moment mt and 2nd order moment gt but they are both decayed over time. Step size is approximately ±α . Step size will decrease, as it approaches minimum

### Early Stopping

### Random Shuffling

### Batch Normalization
