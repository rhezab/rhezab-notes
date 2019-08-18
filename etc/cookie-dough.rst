======================
Cookie Dough Thoughts
======================

This is a place to stash my unbaked thoughts. The way I write makes it sound like I'm sure of myself, but I write that way only beacuse it's easier to write (and read) writing that sounds sure of itself. 

-----------

Achievement
====================

Thinking back on my childhood, my biggest motivation was achievement. I wanted to achieve things. This may be a little surprising to those who knew me as a kid, since I was also kind of a slacker. I'm not saying I worked hard, or did lots of things. All I'm saying is that I believed the reason to do things was to achieve, whatever that means. 

I was handed lots of arbitrary objectives, and I became decent at achieving arbitrary objectives. I got pretty good grades, for instance. But achieving for the sake of achievement isn't very satisfying. 

I guess I'm writing this as a personal resolution to make myself more sensitive to other kinds of rewards, and not let achievement or pretention get in the way. Intrinsic rewards seem promising, rewards that are more ends than means. Rewards like curiosity, or sensual pleasure, or those derived from empathy.

I fantasize about the following scene. It's thirty years in the future. I meet someone who reminds me of a younger version of myself. They ask me why I do x or y. I stare back at them, a little confused. I'm not sure. I stutter. Just because, I guess.


*8/18/19*


-----------

Breeding
=====================

Say you want to design via optimisation. You define a notion of good, and (let's assume) it's magically achieved. How do you define good? 

Defining good is hard. Try it. What, for instance, is a good house? How do you define beauty? 

We may not be able to define beauty, but we can feel it when we see something beautiful. This is the rationale behind breeding. We may not be able to define good, but given several things, we can choose which things are better than others.

The simplified breeding algorithm is simple. At each point in design space, you sample several directions, and choose the most promising ones. You move in a promising direction, and sample again. If you do this over and over again, you should end up with a point in design space that is better according to your implicit notion of good. If at every point on a hill, you walk up, you're going to end up higher than where you started (a physical analogy stolen from gradient ascent). 

Breeding is an optimisation algorithm that doesn't require an explicit objective. It only requires that you know good when you see it. It works. Dogs aren't super cute by accident. 

I wrote this in reflection of `Ganbreeder <https://ganbreeder.app/>`_ and Joel Simon's `talk <https://www.youtube.com/watch?v=8L1bNz4YYjg&t=1s>`_ on Ganbreeder and other things. By the way, I still think it's useful to try to explicitly define good, but that's a topic for another time.


*8/16/19*


-----------

Algorithms, not Pencils
=========================

Art and design projects involving `GANs <https://philippschmitt.com/work/chair>`_ have been pretty hot recently. And while I find them cool, I tend to find them less interesting than other computational projects such as `Evolving Floorplans <https://www.joelsimon.net/evo_floorplans.html>`_ and `Hyphae Lamps <https://n-e-r-v-o-u-s.com/shop/generativeProduct.php?code=99>`_. 

I think I finally understand why. GANs, and other generative models from machine learning, model distributions. In the case of design projects involving them, they model the distribution of existing human designs. We can then reach novel designs by interpolating on the learned manifold of existing designs.

The projects I find more interesting say screw it, we don't care about existing human designs, which is really exciting for two reasons. 

It's exciting because you're not constraining yourself to the manifold of existing human thought.

It's exciting because you're not constraining yourself to old design mediums. More specfically, the projects I find cool design via algorithms rather than pencils -- and this step up the ladder of abstraction means you can achieve previously unmanagable levels of complexity. 

Designing with algorithms give rise to many opportunities for creativity. How do you parameterise your design? How do you translate parameters (genotype) to an actual object (phenotype)? If you're optimising your design for some definition of good, how do you measure your definition of good? How do you define good?


*8/16/19*

