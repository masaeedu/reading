# Programming

## Curry-Howard correspondence

- [A Formulae-as-Types Notion of Control](http://citeseerx.ist.psu.edu/viewdoc/download;jsessionid=539A05FBC2F509D4F2DF59702F69566E?doi=10.1.1.26.6893&rep=rep1&type=pdf)
- [Classical vs constructive logic](https://www.andrew.cmu.edu/user/avigad/Teaching/classical.pdf)
- [Modal logic (order goes propositional logic -> predicate logic -> modal logic)](https://en.wikipedia.org/wiki/Modal_logic)
- [Kripke semantics](https://en.wikipedia.org/wiki/Kripke_semantics)

## Type systems

- [Singleton types are sufficient to model CoC](https://www.iro.umontreal.ca/~monnier/comp-deptypes.pdf)
- [Naive Computational Type Theory](http://www.nuprl.org/documents/Constable/naive.pdf)
- [Predicativity](https://math.stanford.edu/~feferman/papers/predicativity.pdf)
- [Generic type-safe diffing and merging of mutually recursive datatypes (arianvp)](https://docs.google.com/presentation/d/1D9SA7_kU9RZyh0r4LF7kYvn5gDo5uKM9DWIvtUf5MkI/edit#slide=id.g59cdfdc22e_0_35)
- [Epigram: Practical Programming with Dependent Types](http://www.e-pig.org/downloads/epigram-notes.pdf)
- http://philsci-archive.pitt.edu/11079/1/Identity_in_HTT_public.pdf
- [Responsive compilers](https://www.youtube.com/watch?v=N6b44kMS6OM)
- [Extensions and Applications of Higher-Order Unification](http://conal.net/papers/elliott90.pdf)
- [Recovering Purity with Comonads and Capabilities](https://www.cl.cam.ac.uk/~nk480/popl20-cap-submission.pdf)
- [A Lazy Language Needs a Lazy Type System](https://arxiv.org/pdf/1612.04610.pdf)
- [Dependently Typed Records for Representing Mathematical Structure](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.35.9569)
 - [Inductive families](http://www.cse.chalmers.se/~peterd/papers/Inductive_Families.pdf)
 - [Generic level polymorphic n-ary functions](https://gallais.github.io/pdf/tyde19.pdf)
 - [λμ calculus - An algorithmic interpretation of classical natural deduction](https://www.cs.ru.nl/~freek/courses/tt-2011/papers/parigot.pdf)
 - [Syntax and Semantics of Quantitative Type Theory](https://bentnib.org/quantitative-type-theory.pdf)
 - [On the Size of Machines (Blum Size Theorem)](https://www.dropbox.com/s/93727ua10ccv8f5/sizethm.pdf)
 - [Type is an extensible GADT](https://blog.poisson.chat/posts/2018-07-09-type-gadt.html)
 - [Isomorphic Reasoning: Counting PolymorphicType Inhabitants](https://github.com/cohomolo-gy/Isomorphic-Reasoning)
 - [Counting type inhabitants](https://alexknvl.com/posts/counting-type-inhabitants.html)
 - [A Foundation for GADTs and Inductive Families - Dependent Polynomial Functor Approach](https://www.cl.cam.ac.uk/~mpf23/papers/Types/gadtif.pdf)
 - [Giving Haskell a Promotion](https://www.seas.upenn.edu/~sweirich/papers/tldi12.pdf)
 - [Substructural Type Systems](http://mitp-content-server.mit.edu:18180/books/content/sectbyfn?collid=books_pres_0&id=1104&fn=9780262162289_sch_0001.pdf)
 - [A Hands On Introduction to Cubical Type Theory](https://homotopytypetheory.org/2017/09/16/a-hands-on-introduction-to-cubicaltt/)

### Module systems

- [Modular implicits](https://arxiv.org/pdf/1512.01895.pdf)
- [Modular typeclasses](https://www.cs.cmu.edu/~rwh/papers/mtc/short.pdf)
- [Polymorphism, Subtyping, and Type Inference in MLSub](https://www.cl.cam.ac.uk/~sd601/papers/mlsub-preprint.pdf)

### Typeclasses

 - [Type-level instant insanity](https://wiki.haskell.org/wikiupload/d/dd/TMR-Issue8.pdf)
 - [Coherent Explicit Dictionary Application for Haskell](https://lirias.kuleuven.be/retrieve/519822/)
 - [Type Classes Reflect the Value of Types](http://okmij.org/ftp/Haskell/tr-15-04.pdf)

## Parsing

Need to make the parsing stuff I have work on streams of arbitrary tokens rather than just strings (hopefully making it more efficient in the process). Related reading:

- [Streaming library, which provides a ListT-ish thing](https://hackage.haskell.org/package/streaming)
  - [wip stuff for making streaming work for parsing](https://github.com/haskell-streaming/streaming-utils)
- [Invertible syntax descriptions](http://www.informatik.uni-marburg.de/~rendel/unparse/rendel10invertible.pdf)
- [Some kind of simplification of the concepts in the invertible syntax descriptions paper](https://blog.poisson.chat/posts/2016-10-18-typeclass-interface.html)
- [Type-Safe Modular Parsing](https://i.cs.hku.hk/~bruno/papers/sle17.pdf)
- [Parser Combinators for Ambiguous Left-Recursive Grammars](http://richard.myweb.cs.uwindsor.ca/PUBLICATIONS/PREPRINT_PADL_NOV_07.pdf)
- [PEG: Ambiguity, precision and confusion](https://jeffreykegler.github.io/Ocean-of-Awareness-blog/individual/2015/03/peg.html)
- [Derivative parsers](https://arxiv.org/pdf/1010.5023.pdf)
- [Monadic Memoization](http://richard.myweb.cs.uwindsor.ca/PUBLICATIONS/AI_03.pdf)
- [Non-blocking lexing](http://matt.might.net/articles/nonblocking-lexing-toolkit-based-on-regex-derivatives/)
- [agdarsec - Total Parser Combinators](https://gallais.github.io/pdf/agdarsec18.pdf)

I want to be able to associate recursive ADTs with recursive regexen for simple parsing of context free grammars. Here's some relevant resources:

- [From μ-regular expressions to context-free grammars and back](https://www.cs.ru.nl/bachelors-theses/2018/Bart_Gruppen___4465784___From_mu-regular_expressions_to_CFGs_and_back.pdf)
- [Partial Derivatives for Context-Free Languages](https://arxiv.org/pdf/1610.06832.pdf)

## Parallelism

- [A Monad for Deterministic Parallelism](https://cs.indiana.edu/~rrnewton/papers/haskell2011_monad-par.pdf)
- [A Meta-Scheduler for the Par Monad](https://www.cs.indiana.edu/~rrnewton/papers/2012-ICFP_meta-par.pdf)

## Continuations, monads, continuation monads

- [Monadic Reflection in Haskell slides (Andrzej Filinski)](http://cs.ioc.ee/mpc-amast06/msfp/filinski-slides.pdf)
- [Representing Monads 94 POPL paper](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.43.8213&rep=rep1&type=pdf)
- [Capturing the future by replaying the past](https://arxiv.org/pdf/1710.10385.pdf)
- [A monadic framework for delimited continuations](https://cs.indiana.edu/~sabry/papers/monadicDC.pdf)

## Bidirectional programming, optics

- [Taking Updates Seriously (update monad, coupdate comonad)](https://danel.ahman.ee/papers/bx17.pdf)
  - https://www.schoolofhaskell.com/user/edwardk/heap-of-successes
- https://bartoszmilewski.com/2017/07/07/profunctor-optics-the-categorical-view/
- https://arthurxavierx.github.io/RealWorldAppComonadicUI.pdf
- https://danel.ahman.ee/papers/types13postproc.pdf
- [Categories of optics](https://arxiv.org/pdf/1809.00738.pdf)
- [Composing bidirectional programs monadically](https://arxiv.org/pdf/1902.06950.pdf)
- [Lenses for philosophers](https://julesh.com/2018/08/16/lenses-for-philosophers/)
- [Profunctor Optics - A Categorical Update](http://events.cs.bham.ac.uk/syco/strings3-syco5/slides/roman.pdf)

## Testing

- Generative testing
  - [Generating good generators (how to write quickheck tests when it's hard)](https://lemonidas.github.io/pdf/GeneratingGoodGenerators.pdf)
  - [Stack Overflow answer by @lyxia aggregating various resources on generative testing](https://stackoverflow.com/questions/54122466/what-is-the-best-practice-to-generate-data-which-satisfy-specific-property-in-qu)

## Recursion (schemes)

- [Mayer Goldberg: A Variadic Extension of Curry's Fixed-Point Combinator](http://www.ccs.neu.edu/home/shivers/papers/scheme02/article/variadic-y.pdf)
- [Many faces of the fixed point combinator](http://okmij.org/ftp/Computation/fixed-point-combinators.html)

## Zippers

 - https://en.wikibooks.org/wiki/Haskell/Zippers#Mechanical_Differentiation

## Performance
 - [The Worker Wrapper Transformation](http://www.cs.nott.ac.uk/~pszgmh/hackett-thesis.pdf)

## Metaprogramming

 - [Typeable and Data in Haskell](https://chrisdone.com/posts/data-typeable/)

## Lisp

 - [beautifulracket.com blog](https://beautifulracket.com)
   - https://beautifulracket.com/appendix/why-racket-why-lisp.html
   - https://beautifulracket.com/appendix/why-lop-why-racket.html

## Extensible effects

### Free(r) monad

- [Free monad transformers blog post](https://blog.poisson.chat/posts/2017-05-28-free-monad-transformers.html)
- [Free/forgetful functor adjunctions](https://ncatlab.org/nlab/show/free+functor)

Stuff I've played around with so far:

- [Encoding first order extensible effects using the church encoded FreerT](https://github.com/masaeedu/freert-effs)

### Monad transformers

- [Monatron](https://www.fceia.unr.edu.ar/~mauro/pubs/monatron.pdf)
- [Monad transformers as monoid transformers](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.163.4895&rep=rep1&type=pdf)
- [Monad transformers and algebraic effects; what binds them together](http://www.cs.kuleuven.be/publicaties/rapporten/cw/CW699.pdf)
- [Composing monads](http://web.cecs.pdx.edu/~mpj/pubs/RR-1004.pdf)

### Higher order effects

What is the theoretical underpinning of the `polysemy` extensible effects library? My suspicion is that it is a free functor of some kind, probably the free functor from the category of monad transformers to the category of monads.

To answer the question rigorously, I need to do some reading:

- [Extensible effects in scope](http://www.cs.ox.ac.uk/people/nicolas.wu/papers/Scope.pdf)
- [Semantics for algebraic operations](http://homepages.inf.ed.ac.uk/gdp/publications/sem_alg_ops.pdf)
- [polysemy codebase](https://github.com/isovector/polysemy)

### Refactoring
- [Defunctionalization: the best refactoring you've never heard of](http://www.pathsensitive.com/2019/07/the-best-refactoring-youve-never-heard.html)

# Devops

## Nix

- [Nix: under the hood](https://github.com/Gabriel439/slides/blob/master/nix-internals/slides.md)

# Math

## Category Theory

- Futile efforts to keep up with Bartosz Milewski's prolific blog:
  - https://bartoszmilewski.com/2017/12/29/stalking-a-hylomorphism-in-the-wild/
  - https://bartoszmilewski.com/2018/08/20/recursion-schemes-for-higher-algebras/
  - https://bartoszmilewski.com/2019/03/27/promonads-arrows-and-einstein-notation-for-profunctors/
- [All Concepts are Kan Extensions](www.math.harvard.edu/theses/senior/lehner/lehner.pdf)
- [Decisive functors](https://fplab.bitbucket.io/posts/2007-07-08-decisive-functors.html)
  - I suspect that the interaction between traversable and applicative functors can be dualized to an interaction between distributive and decisive functors
- [A whole bunch of abstract algebra structures represented as categories](https://en.wikibooks.org/wiki/Category_Theory/Categories)
- [An investigation of the laws of traversals](https://www.fceia.unr.edu.ar/~mauro/pubs/TraverseLaws.pdf)
- [StackOverflow answer that points to some interesting resources about "directed containers"](https://stackoverflow.com/a/32933842/1726343)
- [Relative monads formalized](https://pdfs.semanticscholar.org/f786/68afed254ea454285924df9ffaf0666c328d.pdf)
- [Trace in symmetric monoidal categories](https://arxiv.org/pdf/1107.6032.pdf)
- [This is the co-end, my only co-friend](https://arxiv.org/pdf/1501.02503.pdf)
- [The Mathematics of Sentence Structure](http://ling.umd.edu//~alxndrw/CGReadings/lambek-58.pdf)
- [Modality via Iterated Enrichment](https://arxiv.org/pdf/1804.02809.pdf)
- [Relating Structure and Power - Comonadic Semantics for Computational Resources](http://drops.dagstuhl.de/opus/volltexte/2018/9669/pdf/LIPIcs-CSL-2018-2.pdf)
- [The Pebbling Comonad in Finite Model Theory](https://arxiv.org/pdf/1704.05124.pdf)
- [From parametricity to conservation laws, via Noether's theorem](https://dl.acm.org/citation.cfm?id=2535867)
- [Joachim Kock's "Notes on Polynomial Functors"](http://mat.uab.cat/~kock/cat/polynomial.pdf) (lots of good stuff on universal algebra and operads and whatnot when you get around to learning those)
- [Theoretical Pearl - Monads from Comonads, Comonads from Monads](http://www.cs.ox.ac.uk/ralf.hinze/WG2.8/28/slides/Comonad.pdf)
- [Bi-actegories](https://www2.irb.hr/korisnici/zskoda/biact.pdf) (stuff related to the equivalent of modules/bimodules but at the level of categories as sets and bifunctors as left/right actions)
  - [Distributive laws for actions of monoidal categories](https://arxiv.org/pdf/math/0406310.pdf)

### Brendan Fong
- http://www.brendanfong.com/
- [The Algebra of Open and Interconnected Systems](https://arxiv.org/pdf/1609.05382.pdf) - apparently there is some good stuff about hypergraphs in here

### Monoidal functors
Need to find some information about things that are between lax and strong monoidal functors: the coherence map for the opposite functor is a retraction/section for the coherence map of the functor, but they do not form a full isomorphism. Some promising search results:

- [Monoidal categories in, and linking, geometry and algebra](https://arxiv.org/pdf/1201.2991.pdf)
- [The problem with Lax Functors (see comments)](https://golem.ph.utexas.edu/category/2009/12/the_problem_with_lax_functors.html)

### Enrichment

My understanding of enrichment still needs a lot of work. I think a good path forward is to study:

1. [A 2-categories companion (some kind of course material explaining 2-categories and bicategories)](https://www.math.uchicago.edu/~may/IMA/Incoming/Lack/companion.pdf)
2. [Basic Bicategories (to understand the concept of a bicategory, a weakening of the definition of a 2-category)](https://arxiv.org/pdf/math/9810017.pdf)
3. ??? (maybe try and represent some monoids objects not in `(,)` as enriched single object categories, and study how monoidal functors interact with them)

## Logic

### Ehrenfeucht–Fraïssé games

- http://www.math.toronto.edu/rossman/EFgames-lecture.pdf
- https://en.wikipedia.org/wiki/Ehrenfeucht%E2%80%93Fra%C3%AFss%C3%A9_game

## Geometry

### Collision detection

I suspect that finding collisions between shapes (or convex hulls of shapes) has something to do with a lattice of shapes under inclusion as binary relation, intersection as meet, union as join.

- [On lattices of convex sets in R^n](https://arxiv.org/pdf/math/0409288.pdf)
- [On Proximity Problems in Open Spaces](https://curve.carleton.ca/system/files/etd/18d4b057-f42a-49e9-b943-ca43ee5cd76d/etd_pdf/ff64c38b3d8b80d6279ddf33bce507fc/barbaflores-onproximityproblemsineuclideanspaces.pdf)

The approach I was considering was to only admit circular subsets of points from a given canvas. Then the meet operation and join operation consists of picking a circle inscribed in the intersection of the two provided circles, and a circle just barely enclosing the two provided circles, respectively. Apparently the latter is a "closure operator", which taking convex hulls is also. The operation of taking the convex hull of the superposition of the provided shapes, when taken as the join operation, actually forms a proper join-semilattice. So maybe this wrapping circle business (or an adjustment of it) does too? Someone pointed out there might be problems with associativity.

Anyway here's a paper about closure operators and lattices:

- [Closure operators on sets and algebraic lattices](https://pdfs.semanticscholar.org/2fc9/320b490cfb8d759f6ec0fb9697434e6ddc78.pdf)

### Graphs

I want to build a 3D git repo visualizer. Need to learn more about graph/tree layout algorithms esp in 3D:

- [Tree Drawing Algorithms and Tree Visualisation Methods (slides)](http://www.it.usyd.edu.au/~shhong/comp5048-lec2.pdf)
- [Cool hyperbolic geometry approach for rendering graphs using a spanning tree](https://graphics.stanford.edu/papers/h3cga/html/)
- [Algebraic Graphs with Class](https://eprint.ncl.ac.uk/file_store/production/239461/EF82F5FE-66E3-4F64-A1AC-A366D1961738.pdf)
- [Directed hypergraphs and applications](https://www.sciencedirect.com/science/article/pii/0166218X9390045P)
- [Algebra of parametrized graphs](https://pdfs.semanticscholar.org/fc44/cab864acb7e5ea07e04018d39f585e02d52c.pdf)

### Vector algebra

I want to render a game of life in toroidal coordinates on an actual torus. I started implementing my own vector algebra library using some generalized n-dimensional vector math stuff, but then became intrigued by what the generalization of the cross product to n-dimensions would be. Turns out this is called the Hodge Star operator. In the course of learning about this, I discovered a rabbithole of interesting things to read:

- [Course on discrete differential geometry](http://brickisland.net/DDGSpring2019/)
- [Wikipedia page on exterior algebra](https://en.wikipedia.org/wiki/Exterior_algebra)
- [TODO: fundamentals even on vector algebra are weak, find some nice resource on this]()
- [Wikipedia page on Hodge star operator](https://en.wikipedia.org/wiki/Hodge_star_operator)

Stuff I've played around with so far:

- [Implementation of game of life using traced comonad (traced probably works out really great for concatenating matrix transforms and doing relative coordinates in nD)](https://ywvr561j8z.codesandbox.io/)

## Topology

@monoidmusician suggested https://mathoverflow.net/questions/19152/why-is-a-topology-made-up-of-open-sets as an entrypoint into topology stuff.

# Misc. blogs

- https://alexknvl.com
- https://coot.me/
- https://bartoszmilewski.com/
- https://adereth.github.io
  - https://adereth.github.io/blog/2015/02/02/poisonous-shapes/
