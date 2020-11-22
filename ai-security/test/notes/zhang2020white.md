# Fairness test on Adversarial samples(AS)
discriminatory instance: one protected attribute lead to diff label which should be impossible.

## Motivation

1. DNN bias problems are more hidden than traditional ones. 
2. Current fairness testing works are on ML and not work well on DNN.
   
## Effect

1. Based on gradient generating way ADF to find the bias cases (like AS)
2. ADF works 2-7 times more efficient than AEQUITAS and Symbolic Generation and can work on also DL framework.

## Details

1. ADF contains a global generation and a local generation. The output of global will be used as input in local. Global is try to identify near the decision boundary.
2. In global part add perturbation on data(add 1 or minus 1), the goal is to maximize the diff between two outputs.
3. In local part, try to find more instances have similar discriminatory. For given discriminatory instance pair, search by normalization gradients.
4. THEMIS explores the input through random sampling；AEQUITAS use random at first then add perturbation (on non-protected attibutes) to find more examples. SG uses symbolic execution. It builds a decision tree to approximating the ML model. 
5. RQ1: effective; RQ2: effecient; RQ3: useful(improve models fairness in training)