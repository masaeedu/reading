# Functional programming

## Extensible effects

### Higher order effects

What is the theoretical underpinning of the `polysemy` extensible effects library? My suspicion is that it is a free functor of some kind, probably the free functor from the category of monad transformers to the category of monads.

To answer the question rigorously, I need to do some reading:

- [Free monad transformers blog post](https://blog.poisson.chat/posts/2017-05-28-free-monad-transformers.html)
- [Monad transformers and algebraic effects; what binds them together](http://www.cs.kuleuven.be/publicaties/rapporten/cw/CW699.pdf)
- [Extensible effects in scope](http://www.cs.ox.ac.uk/people/nicolas.wu/papers/Scope.pdf)
- [Monad transformers as monoid transformers](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.163.4895&rep=rep1&type=pdf)
- [Semantics for algebraic operations](http://homepages.inf.ed.ac.uk/gdp/publications/sem_alg_ops.pdf)
- [Monatron](https://www.fceia.unr.edu.ar/~mauro/pubs/monatron.pdf)
- [polysemy codebase](https://github.com/isovector/polysemy)

Stuff I've played around with so far:

- [Encoding first order extensible effects using the church encoded FreerT](https://github.com/masaeedu/freert-effs)

## Vector algebra

I want to render a game of life in toroidal coordinates on an actual torus. I started implementing my own vector algebra library using some generalized n-dimensional vector math stuff, but then became intrigued by what the generalization of the cross product to n-dimensions would be. Turns out this is called the Hodge Star operator. In the course of learning about this, I discovered a rabbithole of interesting things to read:

- [Course on discrete differential geometry](http://brickisland.net/DDGSpring2019/)
- [Wikipedia page on exterior algebra](https://en.wikipedia.org/wiki/Exterior_algebra)
- [TODO: fundamentals even on vector algebra are weak, find some nice resource on this]()
- [Wikipedia page on Hodge star operator](https://en.wikipedia.org/wiki/Hodge_star_operator)
