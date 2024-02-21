# Tensorflow
- tf.constant()
- Tensor => simply referred as array
- Normal tf.Tensor objects are immutable. To store model weights (or other mutable state) in TensorFlow use a tf.Variable.

- Data structures : tf.Tensor, tf.Variable, tf.TensorArray
- Primitive APIs: tf.shape, slicing, tf.concat, tf.bitwise
- Numerical: tf.math, tf.linalg, tf.random
- Functional components: tf.function, tf.GradientTape
- Distribution: DTensor
- Export: tf.saved_model


  

  - 

### Tensorflow commands
- tf.Constant()
- tf.Variable()
- tf.matmul()
- tf.Tensordot()
- with tf.GradientTape () as tape:
- @tf.function decorator to compute fast (computational graph)
# Keras 
- It is a high level
- It is a Python API
- The base Layer class (A Layer encapsulates a state(weights)   some computational

- tensorflow.keras.sequential() # executes layer by layer in FNN or CNN
- tf.dense() #It is Fully connected Layer In each layer, a output node is connected to all input nodes
- Syntax: tf.keras.Sequential([layer.Dense(25, activation=relu)])
