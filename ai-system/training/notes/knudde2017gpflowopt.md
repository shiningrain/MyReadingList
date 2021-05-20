## gpflowopt

### Motivation
1. Existing opensource lib lacks extensive doc or rigorous testing, it is hard to use new modeling strategy.

### Challenge
1. Create a straightforward interface

### Details
1. Using GPflow as framework ( which is based on tensorflow)
2. Key feature:
   1. support for multi-objective objective functions along with an implementation of an acquisition function specifically for this type of applications
   2. the rigorous testing suite resulting in a code coverage of 99% 
   3. extensive documentation