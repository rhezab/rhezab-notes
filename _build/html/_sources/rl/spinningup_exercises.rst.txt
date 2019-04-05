=====================
Spinning Up Exercises
=====================

Documenting solutions as I work through `Open AI's Spinning Up exercises. <https://spinningup.openai.com/en/latest/spinningup/exercises.html>`_ I won't be writing down every detail of every solution, but rather what I see as the key insights to each exercise. If you're reading this, I'd really appreciate corrections and/or improvements. 

P-Set 1: Basics of Implementation
=================================

.. admonition:: Exercise 1.1: Gaussian Log-Likelihood

    - Key is to realise that a diagonal multivariate Gaussian is just a univariate Gaussian along each component
    - Since each component is independent, we can treat the probability of an n-dim obervation as the product of the probability of each component
    - Calculate component-wise before summing to potentially make use of parallelism

.. admonition:: Exercise 1.2: Policy for PPO

    - Just need to get familiar with TF API
    - MLP solves regression problem of input state to mean action of Gaussian

P-Set 2: Algorithm Failure Modes
=================================

.. admonition:: Exercise 2.1: Value Function Fitting in TRPO

    - TRPO is an advantage-based function (advantage is how much better off you are doing action a given state s compared to the average over all possible actions a')
    - Therefore it makes sense that training your value-function would help TRPO do well

