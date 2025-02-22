# Training Autoencoder for LLM Feature Extraction
I've always wanted to try "brain surgery" on LLMs. The idea is to leverage the pre-trained capabilities of an LLM to focus on a specific subject. How could we do this without needing to prompt the LLM directly? Is it possible to "hack" it to adopt a different personality?

To explore these ideas, I tried training an autoencoder while observing the LLM's neurons during inference through multiple runs. The LLM's features are polysemantic, so the plan is to train with a labeled dataset and observe which neurons are firing. For instance, in this case, we want to find the "Harry Potter" neurons in the network and boost those to shift its personality or focus. The autoencoder is used to identify these features, and then we amplify them to observe the outcome. This concept was inspired by Google's Neuronpedia.

# Approach

- Train an Autoencoder: Learn a compressed representation of LLM activations.
- Feature Extraction: Identify neurons correlated with Harry Potter-related tokens.
- Boosting Mechanism: Modify activations at inference time to shift the probability distribution to Harry Potter texts
- Evaluate token probability shifts