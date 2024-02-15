# Convolution
- Binary Image
  - Pixel value is either 0 or 1
- Gray scale Image
  - Pixel value varies from 0 to 255
- Color Image
  - Each pixel contains 3 values of RGB values(R, G, B)
 
- Text data has a temporal relationship, and image data has a spatial relationship
- Video data has both temporal and spatial relations


### Convolution
- Moving the filter over the original image and computing the pixel value of the resulting image

### Pooling 
- maximum value in the kernel in considered the output of the resulting image
- Deeper in the network the number of features quickly grows • It makes sense to summarize these features deeper in the network
  - From a practical perspective, this reduces the number of computations
  - From a theoretical perspective, these higher-level (i.e., global scale) features don’t require a high spatial resolution
- This process is called pooling and works like a convolution, with the kernel replaced by a pooling operation
- There are multiple methods to summarize the features which are commonly used in Convolutional Neural Networks (CNN):
  1. Maximum
  2. Average
  3. L2- Norm
