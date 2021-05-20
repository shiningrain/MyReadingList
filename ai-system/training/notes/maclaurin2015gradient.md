## Gradient-based Hyperparameter Optimization

### Motivation
1. Choose a suitable hyperparameter set is crucial and frusstratingly difficult.
2. Current works are forcus on gradient-free model-based optimization.
3. Gradient guide tuninig need an inner loop of elementary optimization to compute the loss.

### Effect
1. Propose an algorithm that exactly reverses stochastic gradient descent with momentum to compute gradients to all hyperparameters.
2. gradients allow optimization for thousands of hps.

### Details
1. REverse SGD:
   1. output gradient of f(w) with respect to initial weight w1 and learninig rate, momentum schedules.
   2. But will fail because the reverse gradient descent operations will lose information. Optimize will lead to lost informations.
2. discared entropy storage
   1. when decay $\gamma$ is 0.5, need to storge one bit, 0.25 will increase to 2 bit.
   2. designed an exactly reversible multiplication method to store the message with may lose in division.
3. Experiment
   1. Each meta training need train 100 epoch sgd network
   2. Mnist dataset
   3. hundreds of training
4. Limitation
   1. big lr will lead to gradient uninformative in medium-term training.
   2. Overfit