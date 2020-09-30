# Chapter 3

* Some people think that human psychology naturally works better when it receives information in the form a person in a natural environment would receive it. In this way, working with samples transforms a problem in calculus into a problem in data summary, into a frequency format problem, which is easier to understand.

* We can sample the posterior distribution in order to summarize it:

    * Intervals of defined boundaries: We get the accumulated posterior probabilities within those boundaries

    * Intervals of defined mass: We get the quantiles that accumulate that mass of probability. There are an infinite number of intervals that meet those requirements. We can define, for example, the Highest posterior density interval, which is the narrowest interval containing the specified probability mass.


    * Point estimates: Given the posterior distribution of a parameter, what value should we report? It’s very common to report the parameter value with the highest posterior probability. (Maxima a posteriori or MAP). Another option is to choose a loss function that associates a parameter value with a cost and report the value that minimizes such cost. The key insight here is that different loss functions imply different point estimates. The two most common examples are the absolute loss |d-p|, which leads to the median as the point estimate, and the quadratic loss (d-p)², which leads to the posterior mean as the point estimate. Also, depending on the problem, you could define a unique loss function.

* What do confidence intervals mean? It is common to hear that a 95% “confidence” interval means that there is a 0.95 probability that the true parameter value lies within the interval. In strict non-Bayesian statistical inference, such a statement is never correct, because strict non-Bayesian inference forbids using probability to measure uncertainty about parameters. Instead, one should say that if we repeated the study and analysis a very large number of times, then 95% of the computed intervals would contain the true parameter value.

