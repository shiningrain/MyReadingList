### Twitter Sentiment Analysis

#### Effect

1. The classification performance of the 6 preprocessing methods using 2 feature models and 4 classifiers on 5 twitter data sets for 2 classification tasks


#### Detail
1. Classifier: Random Forest, Naive Bayes, Random Forest, Linear Regression 
2. The baseline is the application of all preprocessing methods, and the effect of preprocessing methods on the effect can be judged by observing the fluctuations in performance  .  Their work lists 9 tables to show the effect of removing one preprocessing at a time...wasting space.
3. Conclusion: URL does not affect the performance of the classifier, stopword and numbers have basically no effect on Ngram.  Negative replacement and expansion of abbreviations can significantly improve performance, and restore repeated letter words causes unstable performance
 