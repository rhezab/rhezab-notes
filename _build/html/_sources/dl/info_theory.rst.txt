========================
Information Theory
========================

I was introduced to information theory in David McAllester's `Fundamentals of Deep Learning class <https://mcallester.github.io/ttic-31230/>`_ (which I loved). The slides are good (but terse - you'll need to put in some work). The problems are excellent (in my humble opinion). 

Chirs Olah's `Visual Information Theory <http://colah.github.io/posts/2015-09-Visual-Information/>`_ is what made information theory "click" for me. The optimal coding interpretation of information theory, and the corresponding visualizations, were extremely helpful to my understanding. The following is a cheat sheet of useful intuitions about definitions in information theory. 

--------

**Entropy.** This is the average code length of the optimal code for a given probability distribution.

.. math::
	H(p)=E_{x\sim p(x)} - \ln p(x) = \sum_{x} p(x) \cdot - \ln p(x)


**Cross Entropy.** This is the average code length if we sample from distribution :math:`p` and communicate using the optimal code for distribution :math:`q`

.. math::
	H(p,q)=E_{x\sim p} - \ln q(x)

**KL Divergence.** You sample from :math:`p`. The KL is how much larger the average code length is when you use the optimal code for distribution :math:`q` as opposed to the optimal code for distribution :math:`p`. 

.. math::
	KL(p,q) 
	&= H(p,q) - H(p) \\
	&= E_{x\sim p} \ln \frac{p(x)}{q(x)} \\
	&\geq 0

**Conditional Entropy.** This is the entropy of r.v. X given that we have observed the state of Y. 

.. math::
	H(X|Y) 
	&= E_{y\sim p(y)} E_{x\sim p(x|y)} - \ln p(x|y) \\
	&= E_{(x,y)\sim p(x,y)} - \ln p(x|y)

**Mutual Information.** How much does X tell me about Y and vice versa? The channel capacity interpretation says that the mutual information tell us how much information X can carry about Y (and vice versa). This interpretation is useful when thinking about rate distortion autoencoders.  

.. math::
	I(X,Y) 
	&= H(X) - H(X|Y)  \\
	&= H(Y) - H(Y|X) \\
	&\geq 0

**Data processing inequality.** Processing data (beyond trivial injective mappings) results in information loss. The proof is quite fun, and provides some insight into why the above (stronger) statement is true. 

.. math::
	\text{For any function f:} \quad  H(f(y)) \leq H(y)


*To be continued with key inequalities and other stuff as I learn it...*		