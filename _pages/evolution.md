---
layout: page
title: Evolution Strategies in Reinforcement Learning
permalink: /evolution/
---

Evolution strategies (ES) belong to a class of nature-inspired optimization methods called evolutionary algorithms developed by H. Beyer in 1989 [1]. These algorithms use adaptation, selection, and recombination of the individuals, which represent possible solutions in order to reach iteratively better solutions. It is important to note that although these algorithms may have been inspired by biological evolution, the mathematical derivations are so abstracted that it is better to think of evolution strategies as a class of black-box stochastic optimization technique for continuous non-linear or non-convex problems [21].

Given a black-box function $$f: D \subset \mathbb{R}^{N_x} \rightarrow \mathbb{R}$$, we are interested in the optimization problem:

$$
\boldsymbol{z}^{\star}:=\underset{\boldsymbol{z} \in \Omega}{\arg \max } f(\boldsymbol{z}),
$$

with $$\Omega \subset \mathbb{R}^{N_x}$$. Instead of solving this objective, we can find the solution to the objective:

$$
\boldsymbol{\vartheta}^{\star}:=\underset{\boldsymbol{\vartheta} \in \Omega}{\arg \max } \mathbb{E}_{p(\boldsymbol{z} \mid \boldsymbol{\vartheta})} f(\boldsymbol{z}),
$$

where $$p(\boldsymbol{z} \mid \boldsymbol{\vartheta})$$ is a distribution on $$D$$ parameterized by the vector $$\boldsymbol{\vartheta} \in \Omega$$. If $$p(\boldsymbol{z} \mid \boldsymbol{\vartheta})$$ can sample points on the maximum of $$f(\boldsymbol{z})$$, then these two formulations have the same solution [4]. The stochastic formulation of the optimization problem enables a rigorous analysis for derivative-free algorithms and allows the incorporation of auxiliary information [4].

In this work, we will consider two different approaches to solve the expectation maximization problem posed in Eq. (2): an exact maximum likelihood solution and a gradient-based approach. In Section 1.1, we derive the expectation maximization optimization problem based on a mixture of weighted samples. In Section 1.3.1 and 1.3.2, taking a Gaussian distribution approach for the sampling distribution, we derive a maximum likelihood solution and, respectively, a maximum a posterior solution. In Chapter 2, we derive different gradient-based methods to solve the expectation maximization optimization problem with a mixture of weighted samples. More precisely, we derive a Stochastic Gradient Ascent-based (SGA) solution, a Natural Gradient Ascent-based (NGA) solution, and a modified Newton-Raphson-based solution (SNM). In contrast to the CMA-ES algorithm proposed by [9], we will implement algorithms as close as possible to the theory and without the use of an evolutionary path, or modifications in the update of the covariance matrix such as the "rank- $$\mu$$ " update [9]. Furthermore, we will test and compare the algorithms on some common benchmark functions for optimization. In the second part of the work, we will investigate the use of evolution strategies with linear policies in the continuous control of the MuJoCo locomotion tasks and compare the performance with the results obtained in [21].


## References

1. H. Beyer, "[Evolution Strategies - A Comprehensive Introduction](https://link.springer.com/article/10.1023/A:1015059928466)", Natural Computing, 2002. 

2. Author(s), "Title of the Paper," Journal Name, vol. X, no. Y, pp. Z1-Z2, Year. [Online]. Available: [Link to Reference 2](http://example.com/reference2).

3. Author(s), "Title of the Paper," Journal Name, vol. X, no. Y, pp. Z1-Z2, Year. [Online]. Available: [Link to Reference 3](http://example.com/reference3).

4. Author(s), "Title of the Paper," Journal Name, vol. X, no. Y, pp. Z1-Z2, Year. [Online]. Available: [Link to Reference 4](http://example.com/reference4).

5. Author(s), "Title of the Paper," Journal Name, vol. X, no. Y, pp. Z1-Z2, Year. [Online]. Available: [Link to Reference 5](http://example.com/reference5).
