### Copycat

#### Motivation
1. Inquiring random data from the target network and establishing a fake data set based on network predictions, imitating the network with the fake data set。
 
#### Detail

1. Use random unlabeled data to query the target network, and use the knowledge of the network to create a pseudo data set using paired input images and output tags.  (Ask the target network and use its calibration data set) Obtaining a data set from the problem domain PD can reduce training costs. 
2. The fake network is trained with a fake data set, and the fake network should be able to achieve similar performance to the target network.  Hypothesis: The attacker chooses to imitate the network structure (without understanding the target structure) using the VGG framework.  Pre-trained models can achieve better results at this stage, using fake data sets for fine-tuning (transfer learning).