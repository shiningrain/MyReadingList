### Sensei

#### Effect

1. Fomalize the data augmentation for DNN with fuzz testing approaches. Implemented 2 demo tools.

2. Evaluate their approach on 15 DNN models with 5 datasets. Their tools can improve the models robust accuracy
obviously.

#### Motivation

1. The current approaches do not work well when there are small perturbations on training inputs or overfit the training dataset.

#### Detail

1. Their method is fuzz testing with GA.
2. They randomly generate the population at the first epoch and then the training robustness. Then they us GA to 
generate the population on purpose.
3. Their method can obviously improve the robustness accuracy on image dataset. The effect is limited on imdb text dataset.

> data argumentation problem --> saddle point optimization problem.