# Keras-Tuner

Python script that demonstrates how to use hyperparameter tuning to determine the optimal number of hidden layers, number of neurons, and learning rate for a neural network used to predict air quality.

## Dataset

The dataset used in this project is the Real_Combine.csv file, which contains air quality data.

## Hyperparameters

The following hyperparameters are used in this project:

- Number of hidden layers
- Number of neurons in each hidden layer
- Learning rate

## Neural Network Architecture

The neural network architecture is defined using the Keras API from TensorFlow. The model is created using a stack of dense layers with the number of layers and number of neurons determined by the hyperparameters. The output layer contains a single neuron with a linear activation function.

## Hyperparameter Tuning

Hyperparameter tuning is performed using the Keras Tuner library. The RandomSearch tuner is used to randomly sample from the search space of hyperparameters. The mean_absolute_error is used as the objective to minimize during the tuning process.

The script tunes the neural network architecture over 5 trials with a maximum of 3 retries per trial. The search space includes a range of 2-20 hidden layers, with each layer containing between 32-512 neurons. The learning rate is chosen from the options 1e-2, 1e-3, and 1e-4.

The data is split into training and testing sets using a 33% test size, and the model is trained for 50 epochs.

## Results

After tuning, the script outputs the results summary of the trials, including the hyperparameters used and the resulting mean absolute error on the test set.
