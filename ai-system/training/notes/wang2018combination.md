# DL hyperparameter optimization

## Motivation
1. Deep learning model is widely used
2. Hyperparameter solution space is too huge to search. Evaluate for one single hyperparameters need too much time
3. current strategy (grid search & random search) is inefficient
4. 


## Effect
1. combine the hyperbind and bayesian. more effective than existing hyperband algorithms.
2. Preform better on hard optimization than other algorithms.

## Detail
1. combine the hyperbind and bayesian.
   1. utilize the previous trial history and focus on really promising ones and avoid wasting time on less promising ones.
2. Bayesian uses a probabilistic surrogate model to avoid the expensive cost in evaluating the trial.
   1. The prediction value of the next sampling point is related to all points in previous trials.
   2. Use TPE as part of the bayesian optimization
