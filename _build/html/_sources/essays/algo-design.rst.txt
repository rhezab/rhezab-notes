===========================
Algorithmic Design
===========================

Here are my thoughts on designing things via designing algorithms, rather than directly designing the thing itself. I'm especially excited about designing optimisation processes. This is also an experiment in writing publicly. Rather than sharing a "complete" series of thoughts, I'm sharing an ongoing process of thinking about algorithmic design.

------

Algorithms, not Pencils
=========================

Art and design projects involving `GANs <https://philippschmitt.com/work/chair>`_ have been pretty hot recently. And while I find them cool, I tend to find them less interesting than other computational projects such as `Evolving Floorplans <https://www.joelsimon.net/evo_floorplans.html>`_ and `Hyphae Lamps <https://n-e-r-v-o-u-s.com/shop/generativeProduct.php?code=99>`_. 

I think I finally understand why. GANs, and other generative models from machine learning, model distributions. In the case of design projects involving them, they model the distribution of existing human designs. We can then reach novel designs by interpolating on the learned manifold of existing designs.

The projects I find more interesting say screw it, we don't care about existing human designs, which is really exciting for two reasons. 

It's exciting because you're not constraining yourself to the manifold of existing human thought.

It's exciting because you're not constraining yourself to old design mediums. More specfically, the projects I find cool design via algorithms rather than pencils -- and this step up the ladder of abstraction means you can achieve previously unmanagable levels of complexity. 

Designing with algorithms give rise to many opportunities for creativity. How do you parameterise your design? How do you translate parameters (genotype) to an actual object (phenotype)? If you're optimising your design for some definition of good, how do you measure your definition of good? How do you define good?


*8/16/19*


------

Breeding
=====================

Say you want to design via optimisation. You define a notion of good, and (let's assume) it's magically achieved. How do you define good? 

Defining good is hard. Try it. What, for instance, is a good house? How do you define beauty? 

We may not be able to define beauty, but we can feel it when we see something beautiful. This is the rationale behind breeding. We may not be able to define good, but given several things, we can choose which things are better than others.

The simplified breeding algorithm is simple. At each point in design space, you sample several directions, and choose the most promising ones. You move in a promising direction, and sample again. If you do this over and over again, you should end up with a point in design space that is better according to your implicit notion of good. If at every point on a hill, you walk up, you're going to end up higher than where you started (a physical analogy stolen from gradient ascent). 

Breeding is an optimisation algorithm that doesn't require an explicit objective. It only requires that you know good when you see it. It works. Dogs aren't super cute by accident. 

I wrote this in reflection of `Ganbreeder <https://ganbreeder.app/>`_ and Joel Simon's `talk <https://www.youtube.com/watch?v=8L1bNz4YYjg&t=1s>`_ on Ganbreeder and other things. By the way, I still think it's useful to try to explicitly define good, but that's a topic for another time.


*8/16/19*