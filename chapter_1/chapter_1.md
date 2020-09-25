# Chapter 1:

- Classical procedures tend to be inflexible and fragile: they often break or are unpredictable when applied to new contexts. So classical tools are not diverse enough to handle many frequent and interesting questions about models or data.

- It’s important to learn how to adapt to new situations and use a logical criteria to deploy new models.

- Hypothesis are not models and many models correspond to the same hypothesis.

- **Falsification does not describe the scientific method correctly**:

    - Models are falsified, not hypothesis, and many models correspond to the same hypothesis.
    - Measurement matters. Even if some data falsifies a model, the methodology that yielded the data is still something to take into account. In reality we have to deal with observation errors, so the idea that we need only one example that contradicts the hypothesis.
    - The hypotheses are often continuous, not binary. So it’s not possible to find “the one” observation that falsifies the hypothesis.

- In the frequentist approach, all probabilities are connected to events in very large samples, so parameters can’t have a distribution, only measurements can (called **sampling distribution**).

- **Interesting example of bayesian vs frequentist approach**:
    - Uncertainty is often related to the measurement itself, and that uncertainty won’t change even if we repeat the experiment infinite times, as a frequentist approach would suggest. The bayesian approach, on the other hand, uses all the information available in the data.
    Galileo saw Saturn through his primitive telescope. Repeating the measurement wouldn’t help to the uncertainty of it.

- **Multilevel model** : we have our model and the model has parameters that often are modeled with a known distribution(prior). If we have a model for the parameter, we have a model inside a model, called a multilevel model.

