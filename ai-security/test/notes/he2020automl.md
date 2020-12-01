## AutoML

## Motivation

1. Design an effective DNN need professional knowledge and great time cost.
2. AutoML is becoming a popular research area and exists many works in 2 aspects: model structure and HPO hyperparameter optimization.


## Effect
1. cover wide range of AutoML. extend the process of data collection to pipeline.
2. detailed comparison of NAS  algorithms from various aspects.
3. summarized unsolved problems and provied future works.


## Details

### Data preparation
1. Data collection:
   1. data synthesis:expand dataset(crop reverse padding rotation; warping and synthetic over-sampling; sentence to foreign language; data simulation(driving);GAN, SDDL(for sentence))
   2. data searching: on web(filter the unrelative data; active learning to avoid wrong labels)
2. Data clean:(standardization qualitative...)
   
### Feature engineering
1. Feature selection
   1. delete the unrelative feature, build a subset,check if the subset effective enough 
   2. searching strategy: complete, heuristic, and random search algorithms
   3. evaluate subset: filter embedded and wrapper
2. feature extraction: PCA, LDA, isomap, autoencoder
3. feature construction: preprocessing

### Model Generation
2 ways to choose model: NAS taditional model selection
1. Model structure:
   1. choose predefined operations
      1. entire based: lacks transferability 
      2. cell based: stack cell structure with good effect. first learn on small dataset and then transform on big dataset. Many works follow 2 hierarchy: inner cell level and outer network level.
      3. progressive structure:incorporating low level cell to generate high level cell.
      4. network morphism: embed no-identity layers and change the depth\width\kernel in one operation.-- increase the training speed.
2. Hyperparameter optimization (HPO)
   1. grid& random search: split the searching space to grids and find the best one then random search
   2. Evvolution-base algorithm: 
      1. encoding schemes: direct and indirect.
      2. strategy: selection;crossover;mutation;update.
   3. Bayes optimization: (traditional is not well in DNN parameters)
   4. Reinforce Learning:
   5. Gradient descent:
3. Model estimation:
   1. Low fidelity:
   2. Weight sharing: the knowledge in previous tasks
   3. surrogate: surrogate model to search the best structure.
   4. early stop: predict the model effect then early stop
   5. resource aware: trade off between effect and cost.

### Future work
1. pipline: current lack of data collection
2. interpretability: no rigorous mathematical proof
3. encode: the encoding strategy in NAS rely on human experience.
4. more area(like on text)
5. learn how to learn not only learn the specific task.