# eva_nn_01
A small multi modal neural network taking image and number as input and output label and sum 

## Description
This notebook illustrated training of a neural network model which takes MNIST digit image and a radom number as an input and predicts the correct label in the image as well as the sum of the digit in image and the random number which has been input. It this illustrates a multi-input and multi output neural network model.

## Data generation strategy
For the purpose of this model we have defined an custom dataset class **NumberMixture** which takes MNIST data set as input and generates the image, a random number, the image label and the sum of radom number and number in image.

##  Model Architecture
The model architecture consists of two inputs - image and number. The image is passed through two convolutional and max pooling layer before extracting vector, the number is passed through embedding layer to get vector representation.

## loss function used

