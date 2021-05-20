## Evolutionary Optimization

### Motivation
1. Activation functions and optimization technique play crucial role in model learninign but often set in heuristic way.
2. Recent automatic reseaches focus on  only one of a large number of components of DL. Not work have optimized both activation and optimizer.

### Effect
1. Propose a genetic method to find optimal fucntions and activations.
2. Encode activation function into parse trees and place them into chromosomes. 

### Details
1. Method:
   1. define the search space about the unary functions and binary functions for x
   2. encoding chromosome: use parse tree to convert, the inner nodes are unary or binary functions; the leaves are operands.
   3. Use roulette wheel selection; In crossover, the optimization and the activation chromosome are no influence to each other; Random select mutation point and build new subtree.
2. configuration
   1. wide resnet model
   2. cifar10 & cifar100 dataset, train 20 epoch
   3. population 40, 100 iteration