### Cradle

#### Effect

1. This is the first tool to detect and localize the multi-backend differences in DL framework (Keras).

2. They do find the bugs by their tool which can lead to negative effect in cross-backends usage.



#### Motivation

1. Keras is widely used. 
2. High level API contains bugs and hard to be found. Existing test can not finish this work well.

#### Detail

1. They detect by the layer output differences (MAD).
2. They localize the problem by the change rate(CR), and use the upper quartile which will lead to lots of false positives.



