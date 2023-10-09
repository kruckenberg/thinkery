# Power of Deep Learning
- (near, approximate) universality: the same mechanisms can learn to approximate any continuous function
# Limitations of Deep Learning
- A model cannot be created without data (how much data?); the data must be labeled (says Jeremy Howard in his book, but I think this isn't true)
- A model can only learn to operate on the patterns seen in the input data used to train it
- Only creates *predictions*, not recommended *actions*

# Over-fitting
Occurs when the model is "memorizing" the training data in a way that doesn't generalize. You'd see the model's validation accuracy getting worse during training. Techniques exist to mitigate over-fitting, but ought not be applied preemptively since they can unnecessarily reduce the model's predictive accuracy. Rule of thumb: deeper architectures are more prone to over-fitting (but with enough data can be significantly more accurate). Coda: (??) choose a network depth appropriate for the size of your dataset. (??) Does this apply to all NN types, or CNN in particular?

# Transfer learning
The most important method for solving problems efficiently (less time, money, and data) is using pretrained models. Using a pretrained model for a new problem space is called **transfer learning**. In brief, you remove the final (output) layer (which was customized to the original training task) and replace it with one or more new layers, initially with randomized weights, as appropriate for the new task.

# Universality
Neural networks are universal in that they can approximate any continuous function. See:
  - Michael Nielsen [A visual proof that neural nets can compute any function](http://neuralnetworksanddeeplearning.com/chap4.html)
  - Links to [other proofs](https://ai.stackexchange.com/questions/13317/where-can-i-find-the-proof-of-the-universal-approximation-theorem) under various assumptions