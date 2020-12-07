## TASO

### Motivation
1. Graph substitution can improve the computation efficiency.
2. Manually substitution has shorts in Maintainability, data layout,  correctness.

### Effect
1. Only need oprator definitions and specifications in automatically generation.
2. Employ fomal verification to ensure the correctness of graph
3. optimize the substitution and data layout.
4. Find bugs in the implementation of graph substitution.
5. High efficiency in experiments on real DNN structures.

### Details
1. Only compare the graph with same fingerprint will reduce the test amount.
2. Enumerating graphs and collect the fingerprints; Test graphs with same FP (output less than little threshould will be equivalent)
3. key idea of verify the graph substitution is to use set of operatior properties to express the first-order logic.
4. TASO will check the property consistency and redundancy. In this process it found some bugs with low cost
5. pruning redundant substitution: input tensor renaming and comon subgraph substitution. After the pruning the substitution reduced 39x
6. TASO will test each operation time on each configuration and hardware, then it will estimate the graph by sum up these
7. 