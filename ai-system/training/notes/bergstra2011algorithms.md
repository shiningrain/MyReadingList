## TPE

### Motivation
1. Traditionally, hyper-parameter optimization has been the job of humans because they can be very efficient in regimes where only a few trials are possible
2. Computer claster and GPU made this be possible to be automatic

### Effect
1. Two effective SMBO algorithm: GP and TPE
2. Find that:
   1. Random search has been shown to be sufficiently efficient for learning neural networks for several datasets, unreliable for training DBNs. 
   2. The sequential algorithms are significantly better than the best previously reported. 

### Details
1. SMBO:
   1. Use the history  x and f(x) to fit the model Mt, and then find the x* with the Mt model by S(...) fucntion. 
   2. S function is a surrogate function which can use less cost to estimate the fx value. Essentially modeling H to approximate f. GP and TPE of this paper all do this work.
   3. Evaluate f(x*) and update the Mt+1 model. 
2. EI criterion:
   1. Integrate the expectation that y is less than the threshold y*
3. GP:
   1. The Gaussian process samples the prior distribution of the final function, and assumes that the prior distribution is a Gaussian process with mean 0 and kernel 1.
   2. in EI criterion, the y* is the min(fx) in history. And it builds the model pM from H to predict the pM(y|x).
4. TPE:
   1. TPE dont use the p(y|x), it choose the p(x|y) and p(y) instead.
   2. TPE transoform the model building process to model the p(x|y). it devide the y space into y < y* and y > y* 2 part. the x desity are lx and gx.( use the observations {x1,x2 ... xn})
   3. In EI the p(y|x)=p(x|y)p(y)/p(x), TPE can get the distribution of EI by this way.
5. Experiment
   1. dataset convex & MRBI
   2. **50 iteration fit the GP model and 200 trial to search the model for DBN** better than manual search used 82 trials and 27 trials.