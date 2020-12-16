## concolic testing

### Motivation
1. The faulty behaviour of DNN wil carries risks, which needs to be validated thoroughly.
2. No existing method implemented concolic testing which combines the concrete execution and symbolic analysis.

### Effect
1. first concolic testing for DNN
2. The implementation has high coverage and can find a lot of adversarial examples.

### Details
1. **alternating between concrete execution and symbolic analysis** to increase the coverage rate.
2. Flow:
   1. generate test input and improve converage.
   2. get test input t and evaluation for the requriement and get t' as test input which is satisfied for the requirement.
   3. test iterated til the satisfactory level of coverage.
3. Test coverage：
   1. Lipschitz Continuity:find the largest diff between v[x1] and v[x2] and smallest diff between x1 and x2
   2. NC: find the layer with max output.
   3. Modified Condition/Decision Coverage: find the closest to the change of activation sign.
   4. NBC: clostest neuron to the boundary(high or low).
4. input: DNN;input t0;heuristic; coverage requirement set
   output: Test set satisfies the coverage requirement