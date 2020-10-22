## Chapter 6

- The aim of this chapter was to describe some of the bad things that can happen when we simply add variables to a regression without having a clear idea of the causal model. Specifically, this are:
    - Multicollinearity
    - Post-treatment bias
    - Collider bias
- The framework developed in this chapter is useful for knowing what variables we must and must not add to a model in order to arrive at valid inferences, but will not help in giving the actual causal model.

- **Multicollinearity** means a very strong association between two or more predictor variables. The consequence of multicollinearity is that the posterior distribution will seem to suggest that none of the variables is reliably associated with the outcome, even if all of the variables are in reality strongly associated with the outcome
- Multiple linear regression answers the question: What is the value of knowing each predictor, after already knowing all of the other predictors?
- When two predictor variables are very strongly correlated (conditional on other variables in the model), including both in a model may lead to confusion. Since both variables contain almost exactly the same information, if you insist on including both in a model, then there will be a practically infinite number of combinations of them that produce the same predictions.
- The problem of multicollinearity is a member of a family of problems with fitting models, a family sometimes known as non-identifiability. When a parameter is non-identifiable, it means that the structure of the data and model do not make it possible to estimate the parameter’s value.
- It is routine to worry about mistaken inferences that arise from omitting predictor variables. Such mistakes are often called **omitted variable bias**. It is much less routine to worry about mistaken inferences arising from including variables. But **included variable bias** is real.

### Common relations between variables

![](https://i.imgur.com/m6XXyLo.png)

- The first type of relation is a **fork:X←Z→Y**. This is the classic confounder. In a fork, some variable Z is a common cause of X and Y, generating a correlation between them. If we condition on Z, then learning X tells us nothing about Y. X and Y are independent, conditional on Z.
- The second type of relation is a **pipe: X → Z → Y**. The treatment X influences fungus Z which influences growth Y. If we condition on Z now, we also block the path from X to Y. So in both a fork and a pipe, conditioning of the middle variable blocks the path.
- The third type of relation is a **collider: X → Z ← Y**. Unlike the other two types of relations, in a collider there is no association between X and Y unless you condition on Z. Conditioning on Z, the collider variable, opens the path. Once the path is open, information flows between X and Y. However neither X nor Y has any causal influence on the other.
- The fourth relation is the **descendent**. A descendent is a variable influenced by another variable. Conditioning on a descendent partly conditions on its parent. In the far right DAG, conditioning on D will also condition, to a lesser extent, on Z. The reason is that D has some information about Z. In this example, this will partially open the path from X to Y, because Z is a collider. But in general the consequence of conditioning on a descendent depends upon the nature of its parent. Descendants are common, because often we cannot measure a variable directly and instead have only some proxy for it.
