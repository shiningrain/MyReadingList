## Deeplocalize
white box, require source code and data.
### motivation
1. Localize the DNN problem is a challenge while the developers are trying to solve the problems
2. Munual debugging cost too much time.
3. Existing solutions (callbacks in keras) cant solve this problem, they cant neither detect the problem effiectly nor localize the problem effectively


### effect

1. First fault localization approach for DNN
2. build a bug-patch benchmarck with 40 kinds of models from Stack overflow and Github


### Detail
1. Two method:
   1. method a: tranlate DL program to imperative program and use probes to capture and save variables
   2. method b: callback function. pass parameters to fit().
   3. Output: Whether have bug and where is it. **Cant repair, need repair manually**
2. In method a, need user translate the codes to specific format/structure.
3. DNN suspect behaviors:
   1. incorrect lr: can be found from gradients/weights;
   2. incorrect input data (e.g., not be normalized or nan): can be found from output variance and mean. or nan and inf
   3. incorrct activation/loss: can be found from loss and accuracy (decrease for nan/inf)
4. Localize:
   1. goal: detect bug/ localize bug/ report fail information
   2. symptoms:
      1. delta weight not correct
      2. loss or accuracy not on correct scale
      3. loss not decreas for accuracy not increase
5. Results:
   1. RQ1: imperative program detect 23/29 bug models; callback detect 34/40; Keras report 28/40
   2. localize 19/29 & 21/40. keras cant localize
   3. RQ2：Low time overhead (lower than keras callbacks)
   4. RQ3：the models cant find/ localize: either predicted wrong labels or have problems in the training dataset, the settings of epoches, batch sizes, the number hidden layers, and the number of neural nodes.