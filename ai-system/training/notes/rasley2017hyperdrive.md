## Hyperdrive

### Motivation
1. Searching for good hyperparams need to face the problems of huge search space, expensive training runtime, sparsity of good
configurations and scarcity of time and resources.
2. Previous works are inefficient and  

### Challenge
1. Efficiently explore hyperparameter values while obtaining high model performance and optimizing time and resource costs.
2. Only few configurations lead to high performance while a majority of configurations perform very poorly

### Effect
1. Efficient algorithm with dynamic scheduling and early temination and implement hyperdrive framework
2. Their algorithm improve 6.7 times than random search and 2.1 times than the best previous scheduling tech.

### Details
1. Design algorithm: 
   1. Early stop the poor configuration(the models whose acc little higher or less than random acc); 
   2. Early Accept the good ones; 
   3. prioritize the promising ones
   4. Start stage: explore; End stage: exploit
2. Using probability model to predict the expect remaining time usage. Terminate the model with too long expected time usage
3. devide the resource into two part to balance the exploit and explore