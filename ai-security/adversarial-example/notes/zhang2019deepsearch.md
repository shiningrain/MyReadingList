# DeepSearch

## Motivation
Constructing query-efficient blackbox attacks is still open and challenging.

## Effect
1. a simple and effective fuzz-based blackbox attack for DNN. And better than other black box attack.
2. show the hierarchical-grouping strategy is effective.

## Detail
### challenge:
1. keep high attack accuracy
2. low queries
> Use the feedback to guide the fuzz to find the decision boundaries. Attack bound by the L-inf

### method
1. They made a proof of linear binary classification. to show how to approach the classification boundary and then extend to nonlinear binary classification.
2. Multi-classification can be divided into several binary classification, and if and only if none of these results in a certain category, it will be classified into that class.
3. If the the adverserial samples are still in searching area, their method will keep decreaset he distance.
4. Hierarchical grouping: for high dimentsional inputs, they devide pixels into different groups and mutate all pixels in the same group once time.
   1. initial grouping:
   2. fuzzing
   3. group split(when the current group can not find the AS, then use the finer granularity.)