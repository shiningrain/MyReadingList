### Confident learning

#### Effect

1. This is the first work researched the impact of simple text preprocessing decisions on the performance of text classifiers (multi-word grouping, Lowercasing, Lemmatizing, etc.) 

2. It propose the preprocess suggestion for training


#### Detail

1. They propose that 1) Lowercasing: May cause confusion between Apple and Apple, increase ambiguity, and reduce system effect. 2) Lemmatizing: The purpose is to reduce sparsity. It is generally used in linear text classifiers and is rarely used in neural network text classification.  3) Multi-word grouping: Strengthen the characteristics of multi-word expression, which may bring better results to training (the call of this method is added to the Word2vector package)