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

poch 0 total_correct_labels: 56311 total_correct_sums: 47795 loss: 494.98781556636095
epoch 1 total_correct_labels: 115021 total_correct_sums: 105978 loss: 118.19812903553247
epoch 2 total_correct_labels: 173965 total_correct_sums: 164563 loss: 96.3456956744194
epoch 3 total_correct_labels: 233023 total_correct_sums: 223265 loss: 87.37342839268968
epoch 4 total_correct_labels: 292141 total_correct_sums: 282005 loss: 86.00667833397165
epoch 5 total_correct_labels: 351343 total_correct_sums: 340919 loss: 76.07689337385818
epoch 6 total_correct_labels: 410619 total_correct_sums: 399908 loss: 70.1180489838589
epoch 7 total_correct_labels: 469822 total_correct_sums: 458700 loss: 79.50271089468151
epoch 8 total_correct_labels: 529089 total_correct_sums: 517693 loss: 74.1352062295191
epoch 9 total_correct_labels: 588396 total_correct_sums: 576713 loss: 69.47311828006059
