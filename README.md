# Handwritten-Digit-Classification-Using-CNN
The objective of this project is to build a image-classifier using Convolutional Neural Networks to accurately categorize the handwritten digits. The data for this project can be found here http://yann.lecun.com/exdb/mnist/
# Convolutional Nerual Networks (CNNs)
Convolutional Neural Networks are a special type of neural networks which are very effective in image recognition and classification. They are powerful as they make use of spatial relationships among the features.

There are four main operations in a typical CNN.

1.Convolution

2.Non Linearity

3.Pooling / Sub Sampling / Down Sampling

4.Fully Connected Layer

To learn more about CNNs, go here https://ujjwalkarn.me/2016/08/11/intuitive-explanation-convnets/.

# Network Architecture
We use three types of layers, in this model. They are the convolutional layers, pooling layers and fully connected layers. For this problem, I have defined the following network architecture.

Note: The input is a sample set of 60,000 images, where each image is 28x28 pixels with 1 channel.

The first layer is a Convolutional layer with 32 filters each of size (3,3) followed by another Convolutional layer with 64 filters each of size (3,3). Then, we have a Max Pooling layer of size (2,2).All the Convolutional layers defined above have ReLU as activation function.

Then there are fully connected layers with 128 units in the first and 10 (no. of o/p units) in the second. The first layer uses tanh as activation function and the second one uses softmax.

I also introduced dropouts in between the stacks of layers to avoid overfitting. The key idea behind dropout is to randomly drop units along with their connections to prevent units from co-adapting too much. Read more https://www.cs.toronto.edu/~hinton/absps/JMLRdropout.pdf.

# MNIST Data
The data can be found and is described http://yann.lecun.com/exdb/mnist/.

# Environment Setup
I recommend using google colab for running the script. 

# Results
I was able to achieve 97.02% accuracy on training data and 92.46% on test data. I encourage you to play with the architecture and the parameters to see what you are able to achieve. Feel free to discuss the same.

# Classifying New Images
The images in MNIST dataset contains only greyscale images and almost all of them are clean. This is because of the purpose the creators had while creating the dataset. So, there is a need for some preprocessing.

First off, the images should be converted to greyscale. This is fairly obvious if you have gone through the training script, where we define the number of channels as 1 in the input format.

Secondly, all the images should be resized to (28,28) for the same reason mentioned above.

Now, you're ready to make predictions on custom images!
