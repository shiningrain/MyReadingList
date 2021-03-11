## PBT
(not opensource)
### Motivation
1. Two common track for huyperparameter tuning has their disadvantages: parallel search need to run model parallelly and sequential optimisation can not run so many times.

### Effect
1. Their algorithm:
   1. Use less time than single optimisation preocess and not need the sequential runs.
   2. Use less resource than random search and grid search.
2. Their method is capable of performing online adaptation of hyperparameters
3. Each traiing run asynchronously evaluate the performance periodically; worse use the current base and modify to search more hyperparams. lead to fast learning and low resources.

### Details
1. training n models as a population using diff hyperparam to optimise.
   1. not use parallel method but use part of the population to adapt the performance
   2. each one in population has two ways:
      1. exploit: adandon current hyperparams and forcus current best (can include the weights of the model)
      2. explore: explore the solution space based on current hyperparams(using noise)
   3. hyperparam: learning rate, entropy cost, and unroll length(specific models)