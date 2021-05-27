## Deeplocalize
**Need build block corpus first**, on MNN framework Tensorflow 1.12
### motivation
1. DL inference quality is hard to test in current strategies.
2. Current fuzzy test depends on manually designing the models. Generating complex graph structured data
automatically and effectively is challenging.

### challenge
1. Generating diversified models to trigger diff structure parts of a given DL engine.
2. Capturinng behaviours of each test. (cant use existing DL neuron coverage criteria)

### effect

1. A method for graph-based fuzzy test. generate digraphs from DL models, which can alleviate the problem of generating diverse dl models.
2. Various model muataion and input mutation
3. operator level coverage criteron and feedback for MCTS to search the most promising blocks.
4. This operator levle coverage guided testing framework improve the effectiveness in **detecting exceptions**


### Detail
1. Definition:
   1. degraph;subgraph;block;block corpus; mutation action.
   2. digraph: G=(V,E), v is conv2d\relu...; e is dataflow
   3. subgraph: used to blocks to define specified structures in testing. G1 is subgraph of G
   4. block: subgraph or operators of NN
   5. block corpus: blocks and attributes(name, range, edge), need to test the block and add the attributs first
   6. mutation action: Ik includes MA(bsk,msk), msk is the mutation operators and bsk is the blocks selection
2. 
   1. Operator type converage (OTC): covered operators amound / total amount in corpus
   2. Input degree coverage (IDC): amount of different input degrees of operator c  in I/ all amount of c in corpus
   3. Single Edge Coverage (SEC)
   4. Shapes&Parameters Coverage(SPC)
   5. Operator-level Coverage (OLC)
3. Maxinum the operator level coverage. mutate the dl model to build lots of test cases.
4. MCTS use to serach the input domain of DL engine
   1. search the potential child nodes untial a leaf node is reached
   2. create childe node c with lowest coverage and operator C is not in path.
   3. generate models using blocks in current path of tree til the terminal conditions
   4. back propagation, highest value in each layer would be the optimal strategy in the test set.
5. Muation selector:
   1.  add/del edge; add/del block
   2.  tensorshape mutation; parameters mutation