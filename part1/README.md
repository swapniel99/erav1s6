# Part 1

![Backpropagation](./images/backprop.png)

[Click here to Download Excel](http://github.com/swapniel99/erav1s6/raw/main/part1/S6%20Part1.xlsx)

[Click here to view in Google Sheets](https://docs.google.com/spreadsheets/d/1NMEAmPLYBT2U-2u5Mkx-RauB0dxvmo8T/edit?usp=sharing&ouid=105619550207509869107&rtpof=true&sd=true)

Backpropagation is used for training neural networks. It involves two main steps: forward propagation (Loss Calculation) and backward propagation (Step Calculation).

### Network:
![Network](./images/network.png)

## Steps
### 1. Forward Propagation:
![Calculations](./images/calc.png)
- We start by feeding an input through the network. In this case, we have an input layer of size 2 where we feed the two inputs i1 and i2.
- Each neuron in the hidden layer takes the weighted sum of its inputs, applies the sigmoid activation function to the sum, and passes the result to the neurons in the output layer.
- Similarly, each neuron in the output layer takes the weighted sum of its inputs (outputs from the hidden layer), applies the sigmoid activation function, and produces the final output values a_o1 and a_o2.
- Ultimately, we compare the network's output to the target output t1 and t2 using the mean squared error loss function.

### 2. Backward Propagation:
![Gradient](./images/gradient1.png)
![Gradient](./images/gradient2.png)
- Here we calculate the gradients of the loss function with respect to the weights and biases of the network.
- Starting from the output layer, we propagate these gradients backward through the network, updating the weights and biases using a technique called gradient descent.
- The update for each weight and bias is determined by the gradient and a learning rate, which controls the magnitude of the update.
- The process of updating the weights and biases based on the gradients is repeated iteratively for a number of epochs or until the network converges to a satisfactory solution.
- The steps of backpropagation involve calculating the partial derivatives of the loss function with respect to the weights and biases in each layer. These partial derivatives are computed using the chain rule of calculus, which allows us to propagate the gradients backward through the network.

By iteratively adjusting the weights and biases based on the gradients, backpropagation helps the neural network learn the appropriate parameters to minimize the loss function and make accurate predictions.

## Effects of learning rate
- Up to a certain limit increasing learning rate increases convergence rate. It even starts achieving 0 loss after LR=2.

![Gradient](./images/lowerLR.png)

- But after that increasing learning rate causes the network to have trouble converging. As you can see for LR=1000, loss is permanently stuck at upper ceiling of 0.25 after first step.

![Gradient](./images/higherLR.png)
