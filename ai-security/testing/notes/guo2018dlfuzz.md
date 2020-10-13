### DLfuzz

#### Effect

1. The first differential fuzzing testing framework aiming to maximize the neuron coverage and works better than DeepXplore

#### Motivation

1. The current researches spend too much time on testing the DL model or in a heavy whit box manner.

#### Detail

1. Their method is from se fuzz testing which setting a seed list and update it when found the coverage improvement.
2. Their loss function aims to decrease the true label logits and improve the NC.
3. They select 4 strategies for neuron selection: frequently/unfrequently coverage in the past, top weight neurons, near the activation threshold.