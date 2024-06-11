# seating-arrangement-neural-network
Optimizing seating arrangements with neural networks

<div align="center">
    <img width="40%" src="https://github.com/faezeh-gholamrezaie/seating-arrangement-neural-network/blob/main/EfficientSeating.jpg">
</div>

## Project Description:

This repository hosts a solution for optimizing seating arrangements using neural network techniques. The neural network is trained to select seating orders that minimize discrepancies among individuals, promoting fair and efficient allocation of seats in scenarios such as classrooms or events.

## Input Data
The neural network takes a matrix as input, denoted as seating_order_conflicts, with values ranging from 0 to 4. This matrix represents the conflicts each individual has with their neighbors. Each person can have up to 4 neighboring conflicts, hence the values range from 0 to 4.

## Model Architecture
The model architecture comprises a neural network with two layers.


## Loss Function
A custom loss function is implemented to calculate penalties based on the probability of each individual's compatibility with their assigned seat. This probability reflects how well-suited the person is to their seat. The loss function multiplies these probabilities for incompatible individuals seated together, penalizing the model more for seating highly incompatible individuals together.

## Training Process
During training, the seating order matrix is initialized randomly. The model then learns to optimize seating arrangements by minimizing the loss function. Individuals with nonzero conflict scores are swapped with each other iteratively to improve compatibility. Once only one incompatible individual remains, the training process is considered complete.


