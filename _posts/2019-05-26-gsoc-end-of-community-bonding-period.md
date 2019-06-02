---
layout: post
title: GSoC - Community Bonding Period Ends !!
subtitle: The Journey will begin now !!
bigimg: /img/path.jpg
tags: [gsoc, sympy, cbp]
---

The all-important `Community Bonding Period` ends!! During these three weeks, I have come to learn a lot more things about SymPy, and especially its `Series` module, the module I would be improving this summer. The first week of the CBP was wasted since I had college exams going on, and couldn't focus. After they ended, I set my blog, and had a meeting over Hangouts with **Sartaj**. 

The meeting ended with the following plan of action to be done in the CBP :-

   - Currently, I will try to understand about the inheritance methodology of Formal Power Series, the algorithm behind computing Formal Power Series, and the logic behind improving the XFAIL tests.
   - I will also try to deduce means to include `composition, and coefficient sequence of power of fps as operations` on fps.
   - Get familiarized with the documentation style of SymPy.
   - `Gitter` will be the primary channel of communication. I will soon add my blog to `planet-sympy` as well.
   
I started by thinking about the `XFAIL` tests which were about `functions having symbolic terms in test_formal.py`. Previously,
```
fps(x**n*sin(x**2),x).truncate() gave rise to a Value Error.
```
So, I thought of splitting the `x**n` term from the function itself, use the rest of the portion to compute the `fps` accordingly, and then multiply the symbolic term in the `xk` (powers of x) and `ind` (independent term) respectively.

   - I made a [PR #16869](https://github.com/sympy/sympy/pull/16869) incorporating those changes. It's a `WIP Pull request`, since the code was too nested and heuristic changes had to be modified.
   - I also read `Wikipedia articles` for implementation of convolution, composition and coeff. of power sequence of fps. I will try to implement this the following coding week.
   - I read the official **SymPy** documentation of the `series` module.
   
   All in all, this was a great phase. Had some constructive discussions with Sartaj as well. Looking forward to the next enchanting phase, the **Coding Period** (Phase 1). Till then, adios !!
