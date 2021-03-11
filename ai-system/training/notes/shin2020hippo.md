## hippo
(not opensource)
### Motivation
1. Hyperparams affect the model training quality a lot
2. Searching suitable hyperparams need large gpu and cost a lot of time.

### Effect
1. Hippo, hyperparam optimization system, can find redundant computation and reused tyhe duplicate workload
2. stage tree(hyperparam config) to reuse hte redundant compuatation
3. Experiment popular dl models and 40 GPU, use much less time. 

### Details
1. hyperparam: learning rate, drop-out ratio, optimization algorithm, momentum,batch size, image augmentation parameters,  training image input size, and input sequence length
2. different training may have same stage in the training process, therefore they build the stage tree.
3. They also create a search plan using different fields in config. when the training hyperparam need to be change, they will create a new config as copy backup.