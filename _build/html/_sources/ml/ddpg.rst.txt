===================================
Deep Deterministic Policy Gradient
===================================

Pseudo-code from `Spinning Up <https://spinningup.openai.com/en/latest/algorithms/ddpg.html#>`_, and accompanying comments for future review. DDPG is an algorithm, specifically adapted for continous action spaces, for learning a Q-function and a corresponding deterministic policy. 


.. figure:: ./images/ddpg_pseudocode.svg
	:align: center

	(Deep Deterministic Policy Gradient, Spinning Up, Open AI)

- **Idea:** We interleave learning a Q-function with learning a policy to "boostrap" us off the ground.
- **Line 2:** Target parameters are essentially copies of previous parameters. They're kept to prevent potential instability in the gradient update on line 13. If the "target" had the same parameters, a possible failure mode might be that we fit the "target" to our Q-function rather than the other way around. 
- **Line 4:** Noise is added the policy at train-time to maintain exploration
- **Line 7:** We maintain a replay buffer in order to stop the Q-function from forgetting how to judge "bad" off-policy states and actions - forgetting such "bad" states can cause the policy to repeat "bad" actions. 
- **Line 14:** This is the line that makes DDPG specifically adapted for continous action spaces. The idea is that we want to solve :math:`a^{*}(s) = argmax_{a} Q(s,a)` via gradient ascent since brute force search is clearly intractable for continous action spaces. But instead of doing gradient ascent everytime we want to perform an action, we train a model according to the objective  :math:`\theta ^ * = max_{\theta} Q(s,a)`. 
- **Line 15:** In practice, :math:`\rho` is often very close to 0
