### Emotion recognition

#### Effect

1. They propose a bi-lstm structure, focus on processing emoticons and hashtags, etc. The model is significantly better than the baseline model (logistic regression)

#### Detail

1. They tried a variety of embedding: word2vector, glove, elmo, sentence embedding; after embedding, there are several bi-lstm hidden layers, each with 1024 neurons; regularization cannot improve over-fitting, so use dropout and Gaussian  Noise reduction over-fitting 
2. The data set is an emotional task data set, including six types of emotions.
3. The compare the effects of different model structures on different embeddings (256,2\*256,1024,2\*1024) 
4. They compare the effects of not using preprocessing, text cleaning, expression preprocessing, label processing, and all combinations