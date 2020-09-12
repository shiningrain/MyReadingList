### High acc & fidenlity

#### Effect
1. Systematically analyzes the limitations of current learning-based extraction attacks and proposes a more effective method.  
2. Propose functionally equivalent extraction, and design a technology that can equate a 10w parameter model to a 2-layer ReLU model

#### Motivation
1. Model extraction should ensure high fidelity while ensuring high accuracy.

#### Detail
1. In learning-based extraction, they proposed to use labeled data and unlabeled data to mix query and learn the target model.
2. In the functional equivalent extraction, they designed an algorithm to calculate the gradient change point of each relu neuron separately by changing the input and then calculate the value and symbol of each layer, finally infer the equivalent model of the two layers of relu.  This method can achieve more than 99% fidelity.