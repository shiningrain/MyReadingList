### Cloudleak

#### Effect
1. Real-world attacks that are difficult to detect with existing defense methods
2. Little queries and low cost ($2 for 76.05% accuracy) brings high accuracy extraction.

#### Motivation
1. Model extraction is a practical attack which can get a good model with low cost. This can harm the victim’s property and even privacy.

#### Detail
1. They use the adversarial sample to query the target model to quickly obtain the judgment boundary of the model and then perform local training on the local models zoo, and finally obtain a well-performed model.
2. They use a feature-based adversarial example generation method with can get a little better result than CW method.