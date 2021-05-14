# Image Recognization Practice
This repository is a Keras practice in image recognization. It is an Assignment for AI coursework.

The data I used is from [OpenML mnist_784 database](https://www.openml.org/d/554) which includes handwritten digits with 784 features.

It includes model training and Hyperparameter tuning.

It starts with model building with Convolutional Neutral Network. I chose the Relu function for the activation function for the hidden layer and the softmax function for the output layer.

Hyperparameter tuning include tuning in several parts:

- **Optimizer:** I tried **SGD, Nesterov Momentum SGD and Adam**. For SGD, I use epochs = 150, which means the model trains 150 times. And for the other two, I decreased the epochs to 60, since they are approaching faster.
- **Dropout rate:** It means how much data you randomly drop in each dropout layer to avoid overfitting. I tried the dropout rate 0.1,0.2,0.3,0.4,0.5,0.6,0.7,0.8 and 0.9.
- **Learning rate:** It means how fast the model learn (how many weight changes after each training). I tried the learning rate 0.01,0.001 and 0.0001.

I used the **Kerastuner** with randomsearch method to get the optimized hyperparameter value. Detailed about Kerastuner can be found [here](https://keras-team.github.io/keras-tuner/).

Detailed Model and tuning process can be found in [here](code.ipynb).
