# Rice Image Classification using Convolutional Neural Networks (CNN)

This repository contains the implementation of a Convolutional Neural Network (CNN) for the classification of rice images into various categories. The model is designed to identify and categorize different types of rice based on images, leveraging deep learning techniques.
The CNN model is built using multiple convolutional layers followed by Leaky ReLU activation, max-pooling layers, and fully connected dense layers.

The architecture of the model is the following:
- Rescaling Layer:
    Rescaling(1./255, input_shape=(val, val, 3))
    This layer normalizes the pixel values from a range of [0, 255] to [0, 1] by dividing each pixel value by 255. This step is crucial for improving the model’s stability and convergence speed;
- First, second and third layer:
    32, 64 and 128 convolutional filters 3x3, with the LeakyReLU with alpha 0.15 and maxpooling 2d to retaining only the most important feature;
- Flatten layer:
    flatten the output in a 1D vector;
- First and second Dense layer:
    Fully connected layers with Leaky ReLU activation function and dropout to prevent overfitting
- Output layer:
    final layer with 5 neurons, corrisponding to the 5 classes of the dataset
  We used Adam optimizer, and Sparse Categorical Crossentropy as Loss Function
  
   
We've searched the best configuration among 3 different batch size and image size, specific:
image_size = [(32, 32), (64,64), (128,128)]
batch_size = [32,64,128]

License
This project is licensed under the MIT License - see the LICENSE file for details.
