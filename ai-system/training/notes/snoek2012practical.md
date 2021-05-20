## spearmint

### Motivation
1. Traditionally, hyper-parameter tuning is a black art that requires expert experience.
2. Developing automatic approaches is much more appealing.

### Effect
1. New algorithms that take into the variable cost of learning experiments and can run good results with multiple cores for parallel experimentation
2. identify bayesian optimization can practise well for ML algorithms.

### Details
1. Bayes optimization:
   1. build a probalilistic model for fx and exploit this model to predict the next x. Only rely on the local gradient or hessian approximation.
   2. Trade off: Search for mininum non-convex function with relatively few evaluation; Do more computaition
   3. Gaussain process: any finite set of N points induces a multivariate Gaussian distribution on R. The properties of distribution are determined by mean and convariance function.
   4. Acquisition Functions for bayes optimization: xbest= argmin f(xn); It has Probablity Improvement / Expected Improvement / Upper confidence Bound criterions.
2. Practical COnsideration for the bayes optimization.
   1. Should consider the unclear convariance function and time consuming; Also need to run in multi-core parallelism.
   2. Choose a common kernel function
   3. Due to the different training time in each trail, propose to optimizer the expected improvement per second 
   4. parallelizing Bayes optimization : obtain montecarlo acquisition for the unfinised evaluation from the history. (integral of expection)
   5. get better result than TPE in MNIST dataset, training times is less than 100.