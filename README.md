### Why Deep learning, Why not Machine learning
## Machine learning
- Pattern finding, clustering the data
# Problems with machine learning
- Not handle text data, image data
- Overfitting and Underfitting


### machine learning
- Input data => feature extraction (by manual) => Model (Classification/ Regression) => Output
- Vast number of Classifiers

### Deep Learning
- Input Data => feature extraction and classification (automatic model development) => Output
- Representation ML is called Deep Learning
- Limited number of Classifiers
![Screenshot 2024-02-19 134437](https://github.com/Selvam-DG/Deep_Learning_and_NLP/assets/98681717/3218bf65-fd9c-4a75-adf0-02ba91509a48)


- Application:
  - Computer Vision: Object Localization, Face Detection, Object Detection
  - NLP: Semantic analysis,  Word2Vec
  - Speech: WaveNet
  - Text Summarization
  - GamePlay: Alpha Go, Combination Deep Q learning to play Atari
  - Spam detection: Detecting fraud emails
  - Medical data analysis
  - Data Compression
  - Anomaly Detection
  - Digital advertising and customer targeting


### Neural Network
- How NN is better than traditional ML
  - Automatic feature extraction and deriving relation between input to output
  - large data source
  - more computation and GPU
- How is bettre than ML
  - 
- What NN takes 

## Artificial Neural Networks:
- ANN contains multiple layers of artificial neurons.
- The first layer is the input layer (in)and the last layer in output layer(on)
- The rest of the inner layers are referred to as hidden layers.
- These are the layers where magic happens; I mean pooling, subsampling, activation, dropout, convolution, compression of data
### Deep learning
- Basically, we refer Deep learning as Learning done by an Artificial Neural network which has more than one hidden layer.
- The intuition is as deep the network is the deeper representation present in data could be extracted
- Can work well with noisy or incomplete data as well, given enough data to learn the underlying function


### The data propagation in a forward pass is named as Feed-Forward Networks
- Feed Forward Network:
  - A feed-forward neural network is an artificial neural network wherein connections between the nodes do not form a cycle
  - Information flow from input to output
- Dense connected means fully connected
- Output = g( ∑ wi.xi + b )
  - where  g is activation function, wi is weights, xi is input values and b is bias
  - Activation Function:  Linear Unit, Rectified Linear Unit(ReLU), Sigmoid, Tanh , Swish
- Backpropagation:
  - Backpropagation is shorthand for "the backward propagation of errors," since an error is computed at the output and distributed backward throughout the network's layers.
  - Why do we need Backprop?
    - We can’t do gradient descent in deep neural network setting
    - It won’t allow us to update the different layers of neurons simultaneously.
    - Thus it makes the weight update a really time-consuming process overall


## Tensorflow + Keras
- end to end open source machine learning platform
- TensorFlow™ is an open-source software library by Google for high-performance numerical computation
- Its flexible architecture allows easy deployment of computation across a variety of platforms (CPUs, GPUs, TPUs), and from desktops to clusters of servers to mobile and edge devices
- Originally developed by researchers at Google Brain and was being used by internal teams at Google
- Optimized for Deep Neural Networks
- Advantages:
  - Flexibility
  - Portability
  - Research and Production
  - Auto Differentiation
  - Performance


## Convolution
- A  two function is combined to get a result of a single function is simply called convolution
- f(x) * h(x)  = g(x)
- Convolution Neural  Networks are the current state of art model Architecture for image classification
  - CNN applies a series of filters to the raw pixel data of an image to extract and learn high-filters
  - Convolution Layer1
  - Pooling Layer1
  - Convolution Layer2
  - Pooling Layer2
  - Dense Layer1
  - Dense Layer2
  - Logits Layer  - y_predict or y_hat





## Pöoling
- Max Pooling
- Average Pooling
- L2 Norm Pooling

# CNN
- tensorspace.js
- tensor playgroung
# RNN/ Recurrent Neural Networks
# LSTM
