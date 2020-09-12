# The TrojAI Software Framework: An OpenSource tool for Embedding Trojans into Deep Learning Models

### Summary

This paper designed two major Python modules:

1. `datagen` synthetic supervised classification data generation and
   manipulation;
2. `modelgen` generating deep learning models including classification model,
   reinforcement learning model, etc.

Within different configurations, this paper illustrates the `pipeline` module
for automatic generation. Note that this paper **does not** help the attackers
to _design_ a more stealthy trojan or backdoor model but help the researchers to
_generate_ a bunch of data and models based on a specific pipeline
configuration. Taking advantage of the flexible framework, it enables research
into trojan detection and mitigation strategies across the space of all possible
triggers, embedding methodologies, and data and model modalities. 
