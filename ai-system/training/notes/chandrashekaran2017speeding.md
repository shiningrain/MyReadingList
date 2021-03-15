## speed up
Their aim is to terminate the trainings who can not beat the best training so far in the future.
### Motivation
1. Training multi-models has too much time cost and become infeasible.
2. Previous work requires too much preivous builds to make prediction.

### Effect
1. Present a straightforward and simple way to predict the position learning curve will terminate
2. Incorporate this approach with an existing termination criterion algorithm

### Details
1. Object: given previous builds and n epoch in current build, predict the learning curve from n+1... epochs and the futrue performance.
2. Approach: transform the previous builds data to approximately match current build.
3. Build regression model to predict the future curve