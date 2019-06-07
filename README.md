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

Stuff I've played around with so far:

- [Implementation of game of life using traced comonad (traced probably works out really great for concatenating matrix transforms and doing relative coordinates in nD)](https://ywvr561j8z.codesandbox.io/)

## Curry-Howard correspondence

- [A Formulae-as-Types Notion of Control](http://citeseerx.ist.psu.edu/viewdoc/download;jsessionid=539A05FBC2F509D4F2DF59702F69566E?doi=10.1.1.26.6893&rep=rep1&type=pdf)
- [Classical vs constructive logic](https://www.andrew.cmu.edu/user/avigad/Teaching/classical.pdf)
- [Modal logic (order goes propositional logic -> predicate logic -> modal logic)](https://en.wikipedia.org/wiki/Modal_logic)
- [Kripke semantics](https://en.wikipedia.org/wiki/Kripke_semantics)

## Misc type systems

 - [Singleton types are sufficient to model CoC](https://www.iro.umontreal.ca/~monnier/comp-deptypes.pdf)
 - [Naive Computational Type Theory](http://www.nuprl.org/documents/Constable/naive.pdf)
 - [Predicativity](https://math.stanford.edu/~feferman/papers/predicativity.pdf)
 - [Generic type-safe diffing and merging of mutually recursive datatypes (arianvp)](https://docs.google.com/presentation/d/1D9SA7_kU9RZyh0r4LF7kYvn5gDo5uKM9DWIvtUf5MkI/edit#slide=id.g59cdfdc22e_0_35)
 - [Epigram: Practical Programming with Dependent Types](http://www.e-pig.org/downloads/epigram-notes.pdf)

## Misc category theory

- Futile efforts to keep up with Bartosz Milewski's prolific blog:
  - https://bartoszmilewski.com/2017/12/29/stalking-a-hylomorphism-in-the-wild/
  - https://bartoszmilewski.com/2018/08/20/recursion-schemes-for-higher-algebras/
  - https://bartoszmilewski.com/2019/03/27/promonads-arrows-and-einstein-notation-for-profunctors/

- [All Concepts are Kan Extensions](www.math.harvard.edu/theses/senior/lehner/lehner.pdf)
- [Composing bidirectional arrows bidirectionally](https://arxiv.org/pdf/1902.06950.pdf)
- [Decisive functors](https://fplab.bitbucket.io/posts/2007-07-08-decisive-functors.html)
  - I suspect that the interaction between traversable and applicative functors can be dualized to an interaction between distributive and decisive functors

## Parsing

Need to make the parsing stuff I have work on streams of arbitrary tokens rather than just strings (hopefully making it more efficient in the process). Related reading:

 - [Streaming library, which provides a ListT-ish thing](https://hackage.haskell.org/package/streaming)
   - [wip stuff for making streaming work for parsing](https://github.com/haskell-streaming/streaming-utils)
 - [Invertible syntax descriptions](http://www.informatik.uni-marburg.de/~rendel/unparse/rendel10invertible.pdf)
 - [Some kind of simplification of the concepts in the invertible syntax descriptions paper](https://blog.poisson.chat/posts/2016-10-18-typeclass-interface.html)

## Continuations, monads, continuation monads

- [Monadic Reflection in Haskell slides (Andrzej Filinski)](http://cs.ioc.ee/mpc-amast06/msfp/filinski-slides.pdf)
- [Representing Monads 94 POPL paper](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.43.8213&rep=rep1&type=pdf)
- [Capturing the future by replaying the past](https://arxiv.org/pdf/1710.10385.pdf)

## Lenses, optics and their relation to user interfaces

- [Taking Updates Seriously (update monad, coupdate comonad)](https://danel.ahman.ee/papers/bx17.pdf)
  - https://www.schoolofhaskell.com/user/edwardk/heap-of-successes
- https://bartoszmilewski.com/2017/07/07/profunctor-optics-the-categorical-view/
- https://arthurxavierx.github.io/RealWorldAppComonadicUI.pdf
- https://danel.ahman.ee/papers/types13postproc.pdf
- [Categories of optics](https://arxiv.org/pdf/1809.00738.pdf)
