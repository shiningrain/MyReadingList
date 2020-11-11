# testing on confusion and bias of trained classifiers

## motivation
1. Model has two root cause on the mis-classify 1) confusion(mountain and skier) 2)bias (diff result between 2 related groups.)

## effect
1. propose a new NC metric to meature the confusion and bias error in model.
2. find many errors with high precision in wildly used DNN models

## details
1. first construct a metrix which can reflect the neuron activation probability between classes and neurons.
2. the cloumn vectors of the confusioned classes will be close enough.
3. they analyed how the threshold effect the efficiency.