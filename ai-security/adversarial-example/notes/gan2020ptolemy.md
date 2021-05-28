## Ptolemy

### Motivation
1. The Robustness issue obstruct the deployment of DNN in specific domains.
1. Current Adversarial attack detection either cant detect adversarial samples in ingerence-time or have too high overhead

### Effect
1. Propose a system which can detect AS in inference process with low overhead (2% performance overhead) and high accuracy
2. A method which using the runtime path to detect the AS (similar class should have similar path), build path for each input, use DNN program execution characteristics  to detect AS
3. Present a programmable hardware to achieve lowlatency online adversarial defense. 
4. Can even defense the whitebox adaptive attack

### Details
1. Existing method:
   1. include the AS into training set and retrain : require lots of time
   2. use redundancies to defend AS: large overhead, not practical
2. Algorithrm Framework:
   1. insight: right prediction will enable a set of neuron different to other inputs
      1. regard NN as command programs and use neuron set/path to guide the AS detection.
   2. Get the import neurons: most contribution neurons
      1. the last layer at least one; other layers at least $\theta$ of total neurons n.
      2. Then choose the mininum set of neurons, at least contribute  $\theta * n$
      3. The important neurons identified at layer Li are used to determine the important neurons at layer Li−1
   3. Get the path from neurons
      1. use $m_{ij}$ to indicates whether the neuron at layer i position j is an important neuron
      2. P is the bitwise OR operation for m from all correct inputs
   4. generating and appending P in traininig(static); Then it can detect AS for the inputs after generating enough class path
   5. 3 knobs to control how to extract activation path.
      1. Extraction Direction (Forward vs. Backward); Thresholding Mechanism (Cumulative vs. Absolute); Selective Extraction (Start/Termination Layer)
   6. Algorithm: inference--extract important neurons--build class path--compare path and judge.

### Analyze problem/idea/evaluation
1. Idea & Problem:
   1. inefficient trade-off: 10% overhead with 0.03 accuracy.
   2. Need to training & generate the class path first. The detection effect will depend on the data scale.
2. Experiment
   1. have more detection accuracy and less overhead than all detection methods
   2. have capacity to defense the whitebox adaptive attack.

### Future direction

1. Design to deploy in industry environment.
2. Design intelligent search heuristics (e.g., simulated annealing) to find perturbations that meets the hard path constraint while fooling Ptolemy

### Questions
1. How much is their false positive rate / Miss clasiffication, especially for the small models? Seems like the small model will occur more mis classification.
2. Any analysis for FP cases?