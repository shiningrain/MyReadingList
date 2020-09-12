## DNN Property:
Decision patterns are analogous to path constrains in program analysis.
### Motivation
1. DNNs also suffer from a lack of explainability
2. The increased use of DNNs also brings along several safety and security concerns.
### Effect
1. They infer properties corresponding to decision patterns of neurons in the DNN.
### Detail

The basic idea of this paper is that the prediction mode of the output based on the intermediate state is relatively stable, so an intermediate state can be used to predict the output directly.  The article begins with a simple NN to briefly describe the principle, and later explains how their work is implemented in a complex network.