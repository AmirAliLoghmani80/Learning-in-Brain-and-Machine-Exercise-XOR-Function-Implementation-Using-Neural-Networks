# Learning-in-Brain-and-Machine-Exercise-XOR-Function-Implementation-Using-Neural-Networks

This project aims to implement the XOR function using a neural network, comparing two different training methods: **Error Backpropagation** and **Genetic Algorithm**. The XOR function presents a challenge for single-layer networks, so a multi-layer perceptron (MLP) with a 2:2:1 architecture (two hidden neurons and one output neuron) was used to solve the problem.

## Project Overview

The XOR function is a basic yet non-linearly separable problem, making it an ideal case for testing the capabilities of multi-layer neural networks. In this project, we evaluate the performance of two training techniques:
1. **Error Backpropagation**
2. **Genetic Algorithm (GA)**

The goal is to determine which method achieves better results for training the neural network, both in terms of convergence speed and overall performance.

### Key Objectives

- **Network Architecture**: Design a 2:2:1 neural network to solve the XOR problem.
- **Training Methods**: Compare error backpropagation and genetic algorithms for optimizing network weights.
- **Evaluation**: Measure the performance of each method by analyzing convergence speed and accuracy.

## Methods

### 1. Error Backpropagation
Error backpropagation is a supervised learning algorithm used to minimize the error in feed-forward neural networks. The process involves two phases:
- **Forward Pass**: The input data is passed through the network to compute the output.
- **Backward Pass**: The error is propagated back through the network, and the weights are updated using gradient descent to minimize the error.

In this project, the network was trained using:
- **Learning Rate**: 0.1
- **Error Threshold**: Training was continued until the error for each sample was less than 0.4.

### 2. Genetic Algorithm (GA)
The genetic algorithm is an optimization technique inspired by the process of natural selection. The algorithm involves:
- **Initial Population**: A random population of candidate solutions (network weights).
- **Fitness Function**: Evaluates the performance of each candidate solution based on the accuracy of the XOR function.
- **Crossover**: Combines the characteristics of parent solutions to create offspring.
- **Mutation**: Introduces small random changes to maintain diversity in the population.
- **Selection**: The best-performing individuals are selected for the next generation.

In this project, the GA was run for 50 generations, with single-point crossover and random mutation.

## Results

### Error Backpropagation
- **Learning Rate**: 0.1
- **Convergence**: The network converged after several epochs, but the results were sensitive to initial weight settings. In some cases, the method failed to converge efficiently.
- **Threshold**: Outputs above 0.5 were classified as 1, and others as 0.

### Genetic Algorithm
- **Generations**: 50 generations were sufficient for the network to converge to an appropriate solution.
- **Crossover**: Single-point crossover was used for combining solutions.
- **Mutation**: Random mutations introduced diversity to explore the solution space.
- **Performance**: The genetic algorithm converged faster and was less sensitive to initial conditions than backpropagation.

### Comparative Analysis
- **Convergence Speed**: The genetic algorithm reached a solution faster than error backpropagation.
- **Sensitivity to Initial Parameters**: Backpropagation was more sensitive to the initial weights, while the genetic algorithm showed better robustness in this regard.
- **Accuracy**: Both methods successfully solved the XOR problem, but the genetic algorithm demonstrated a more consistent performance.

## Conclusion

This project demonstrates the application of both error backpropagation and genetic algorithms for solving the XOR problem. While error backpropagation remains the most widely used method in neural network training, the genetic algorithm provided faster convergence and robustness to initial weight settings. Each method has its own advantages:
- **Error Backpropagation**: Well-suited for standard tasks and computationally efficient.
- **Genetic Algorithm**: Better for problems where the error landscape is complex and non-convex, or where backpropagation struggles with initial conditions.

The choice between these methods depends on the specific requirements of the task and available computational resources.
