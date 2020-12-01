## Auto keras

### Motivation
1. Network morphism-based NAS methods are not efficient enough.
2. The cost of bayes optimazition (in function explore) is expensive.
3. Third, the changes caused by a network morphism operation is complicated

### Effect
1. autokeras(developed by this work) can find the lowest error in limited time on target tasks
2. better than base-line on benchmark
3. offline autoML for DNN models

### Details
1. An efficient neural architecture search with network morphism which utilizes Bayesian optimization to guide through the search space by selecting the most promising operations each time.
2. Three challenge solved:
   1. edit-distance kernel for NAS space challenge.
   2. optimization with simulated annealing algorithm
   3. group-level morphism for shape consistency

3. 3 experiments: effective in searching; efficient in optimization; kernel function truely effective?