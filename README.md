# eva_nn_01
A small multi modal neural network taking image and number as input and output label and sum 

## Description
This notebook illustrated training of a neural network model which takes MNIST digit image and a radom number as an input and predicts the correct label in the image as well as the sum of the digit in image and the random number which has been input. It this illustrates a multi-input and multi output neural network model.

## Data generation strategy
For the purpose of this model we have defined an custom dataset class **NumberMixture** which takes MNIST data set as input and generates the image, a random number, the image label and the sum of radom number and number in image.

##  Model Architecture
The model architecture consists of two inputs - image and number. The image is passed through two convolutional and max pooling layer before extracting vector, the number is passed through embedding layer to get vector representation.

We further concatenate the output vectors from number and image to create a joint vector (at 3rd last layer) and use the concatenated vector for further image label and number sum classification.



## loss function used
For image label - cross entropy loss function has been used as its a classification problem.
For number sum as the ouptput is being used is one hot encoded vector represeting the 19 possiblities from 0-18, it effectively turns this into a classification problem, hence here also cross entropy has been used.

### training logs

