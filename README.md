# Programming

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
- [Factorising folds for faster functions](https://www.fceia.unr.edu.ar/~mauro/pubs/f5-ext.pdf)

## Zippers

- https://en.wikibooks.org/wiki/Haskell/Zippers#Mechanical_Differentiation

## Performance
- [The Worker Wrapper Transformation](http://www.cs.nott.ac.uk/~pszgmh/hackett-thesis.pdf)
- [Reflection without remorse - A Conceptual Sequence as a Tangible and Efficient Data Structure](http://okmij.org/ftp/Haskell/Reflection.html)

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

## Refactoring
- [Defunctionalization: the best refactoring you've never heard of](http://www.pathsensitive.com/2019/07/the-best-refactoring-youve-never-heard.html)

## Compilation

- [Supercompilation by evaluation](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/07/supercomp-by-eval.pdf?from=http%3A%2F%2Fresearch.microsoft.com%2Fen-us%2Fum%2Fpeople%2Fsimonpj%2Fpapers%2Fsupercompilation%2Fsupercomp-by-eval.pdf)

## Fun concepts

### Backwards programming

It's fun to program with products:

```haskell
assoc :: ((x, y), z) -> (x, (y, z))
assoc ((x, y), z) = (x, (y, z))
```

You can receive everything and throw things away that you don't care about.

It's a little bit tedious to program with coproducts:

```haskell
assocE :: Either (Either x y) z -> Either x (Either y z)
assocE (Left (Left x)) = Left x
assocE (Left (Right y)) = Right $ Left y
assocE (Right z) = Right $ Right z
```

You receive things one case at a time, you can't just ignore cases you don't care about.

I suspect that this has something to do with the fact that Hask is cartesian closed, and the product tensor is `(,)`. But of course Hask has a dual, and in the dual category, it's `Either` that's the product. So maybe if we had some notion of "backwards" pattern matching, it would be fun to use it for coproducts and tedious for products!

After some discussion and googling, I found some promising links:

- https://link.springer.com/chapter/10.1007%2FBFb0018355
- https://homepages.inf.ed.ac.uk/wadler/papers/dual-reloaded/dual-reloaded.pdf
- http://www.cs.ox.ac.uk/ralf.hinze/WG2.8/27/slides/kenichi1.pdf
- http://www.is.ocha.ac.jp/~asai/papers/diku-ist11.pdf
- http://www.cs.ox.ac.uk/people/nikos.tzevelekos/DualCalc_06.pdf

## Probabilistic programming

- [Selective Applicative Functors and Probabilities](https://github.com/bolt12/master-thesis/raw/master/Msc_Thesis___PDR(4).pdf)
- [Algebra of Programming](https://themattchan.com/docs/algprog.pdf)
- [Explanation of probability monad](http://www.cs.ru.nl/B.Jacobs/PAPERS/triangle.pdf). Includes representation of probability distribution as convex sum that I need to use in https://github.com/masaeedu/co-optics to model the generator half of bigenerators. This should allow for an implementation of `Alternative` that is properly associative.

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
- [Dynamic Typing with Dependent Types](https://sip.cs.princeton.edu/pub/TCS04.pdf): Really interesting paper about a gradually typed approach for adding dependent types to fragments of a dynamically typed program
- [Self Types for Dependently Typed Lambda Encodings](https://homepage.divms.uiowa.edu/~astump/papers/fu-stump-rta-tlca-14.pdf)

Are ADTs an essential primitive of a sufficiently expressive dependent type system? Based on how things work out computationally in untyped JS, it would be really nice if the answer was "no". Here are some links that seem to provide promising evidence for that hypothesis:

- http://www.larrytheliquid.com/drafts/generic-elim.pdf
- https://www.ioc.ee/~james/papers/levitation.pdf

### Books

- [Type Theory and Functional Programming](https://www.cs.kent.ac.uk/people/staff/sjt/TTFP/ttfp.pdf)
- [Programming in Martin Lof's Type Theory](http://www.cse.chalmers.se/research/group/logic/book/book.pdf)
- [A Primer on Homotopy Type Theory - Part 1: The Formal Type Theory](http://philsci-archive.pitt.edu/11157/1/HTT_Primer-PART-1.pdf)
- [Homotopy Type Theory](https://homotopytypetheory.org/book/)

### Module systems

- [Modular implicits](https://arxiv.org/pdf/1512.01895.pdf)
- [Modular typeclasses](https://www.cs.cmu.edu/~rwh/papers/mtc/short.pdf)
- [Polymorphism, Subtyping, and Type Inference in MLSub](https://www.cl.cam.ac.uk/~sd601/papers/mlsub-preprint.pdf)

### Typeclasses (and how to avoid their use because they SUCK)

- [Type-level instant insanity](https://wiki.haskell.org/wikiupload/d/dd/TMR-Issue8.pdf)
- [Coherent Explicit Dictionary Application for Haskell](https://lirias.kuleuven.be/retrieve/519822/)
- [Type Classes Reflect the Value of Types](http://okmij.org/ftp/Haskell/tr-15-04.pdf)
- [Simplifying typeclasses](http://h2.jaguarpaw.co.uk/posts/simplifying-typeclasses/)
- [GHC proposal: Allow direct access to underlying concrete class dictionaries](https://github.com/ghc-proposals/ghc-proposals/pull/324)

### Curry-Howard correspondence

- [A Formulae-as-Types Notion of Control](http://citeseerx.ist.psu.edu/viewdoc/download;jsessionid=539A05FBC2F509D4F2DF59702F69566E?doi=10.1.1.26.6893&rep=rep1&type=pdf)
- [Classical vs constructive logic](https://www.andrew.cmu.edu/user/avigad/Teaching/classical.pdf)
- [Modal logic (order goes propositional logic -> predicate logic -> modal logic)](https://en.wikipedia.org/wiki/Modal_logic)
- [Kripke semantics](https://en.wikipedia.org/wiki/Kripke_semantics)

### ADTs

- [Views: A way for pattern matching to cohabit with data abstraction](https://www.cs.tufts.edu/~nr/cs257/archive/phil-wadler/views.pdf)
- [The view from the left](https://dl.acm.org/doi/10.1017/S0956796803004829)

### Dependently typed programming

#### The singletons saga

- [Dependent types in Haskell: Theory and Practice](https://arxiv.org/pdf/1610.07978.pdf) (specifically what I want to get out of this is some kind of guiding principle or idea that underpins the design of `singletons`)
- [Dependently Typed Programming with Singletons](https://cs.brynmawr.edu/~rae/papers/2012/singletons/paper.pdf) ("the singletons paper")
- [Promoting Functions to Type Families in Haskell](https://cs.brynmawr.edu/~rae/papers/2014/promotion/promotion.pdf) ("the promotion paper")
- Something is bad in singletons land, need to understand https://github.com/goldfirere/singletons/issues/150

#### Containers

I have this big stack of concepts I'm trying to work through at the moment that goes like this:

- There is this notion of operad with sets of variadic operations, but with no restrictions on how the operations may be composed (hence _sets_ and not categories)
- I wish to generalize this along two dimensions: I want to describe the arity of a set of operations by a set of input labels instead of a mere natural number, and I want a partial composition operation such that the valid precompositions for a given operation are restricted
- There is this concept of a "colored operad" (aka multicategory), in which we solve the second problem: there is this set of "colors", and the family of operation sets is no longer indexed by a natural number, but instead by lists of colors. Further, composition is restricted so that "output colors" and "input colors" line up.
- Now to go beyond lists and to maps (and maybe to other containers), we need some systematic way of abstracting the relationship between lists and natural numbers to maps and strings
- The theory of "containers" in dependently typed programming elaborates on this relationship between a set of "shapes", each of which corresponds to a set of positions in a container (for lists the set of shapes corresponds to the natural numbers).

Here's some relevant reading:

- [Categories of Containers](https://www.cs.nott.ac.uk/~psztxa/publ/fossacs03.pdf)
- [Indexed Containers](http://strictlypositive.org/indexed-containers.pdf)
- [Generic Programming Within Dependently Typed Programming](https://www.cs.nott.ac.uk/~psztxa/publ/wcgp02.pdf)

### Linear types

- [Propositions as Sessions](http://homepages.inf.ed.ac.uk/wadler/papers/propositions-as-sessions/propositions-as-sessions.pdf)
- [I Got Plenty o' Nuttin'](https://personal.cis.strath.ac.uk/conor.mcbride/PlentyO-CR.pdf)

# Devops

## Nix

- [Nix: under the hood](https://github.com/Gabriel439/slides/blob/master/nix-internals/slides.md)

# Math

## Category Theory

- Futile efforts to keep up with Bartosz Milewski's prolific blog:
  - https://bartoszmilewski.com/2017/12/29/stalking-a-hylomorphism-in-the-wild/
  - https://bartoszmilewski.com/2018/08/20/recursion-schemes-for-higher-algebras/
  - https://bartoszmilewski.com/2019/03/27/promonads-arrows-and-einstein-notation-for-profunctors/
  - https://bartoszmilewski.com/2016/01/21/tambara-modules/
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
- [Initial algebra and final coalgebra semantics for concurrency](http://citeseerx.ist.psu.edu/viewdoc/download;jsessionid=A98BC2E03563145225EDE0ACE2A297E0?doi=10.1.1.28.8093&rep=rep1&type=pdf)
- [A Study of Categories of Algebras and Coalgebras](https://www.andrew.cmu.edu/user/awodey/students/hughes.pdf)
- [Categories of containers](https://www.cs.nott.ac.uk/~psztxa/publ/fossacs03.pdf)
- [Monads and algebraic structures (good explanation of monadicity and Eilenberg-Moore category of a monad)](https://math.uchicago.edu/~may/REU2012/REUPapers/Sankar.pdf)

### Coalgebraic descriptions of systems (state machines)

The theory of "systems" with dynamic behavior is apparently well modeled coalgebraically. So for example a Moore machine is a coalgebra of the signature functor ``, where the carrier represents the state. The terminal coalgebra this unfolds to represents the behavior of the system.

- [Towards a Uniform Theory of Effectful State Machines](https://arxiv.org/pdf/1401.5277.pdf)
- [Statecharts: A visual formalism for complex systems](https://www.inf.ed.ac.uk/teaching/courses/seoc/2005_2006/resources/statecharts.pdf)
- [Coalgebraic Automata and Canonical Models of Moore Machines](https://qubd.github.io/files/CanonicalModelsOfCoalgebraicAutomata.pdf)
- [Universal coalgebra: a theory of systems](https://www.sciencedirect.com/science/article/pii/S0304397500000566)
- [A coalgebraic semantic framework for component-based development in UML](https://www.sciencedirect.com/science/article/pii/S1571066105000411)
- All of Bart Jacobs' stuff, there's a metric crapton of stuff on coalgebras and systems [here](https://scholar.google.com/citations?user=c2b9xloAAAAJ&hl=en), most of which is referenced in the other papers in the list
  - [A Bialgebraic Review of Regular Expressions, Deterministic Automata and Languages](https://repository.ubn.ru.nl/bitstream/handle/2066/36207/36207.pdf?sequence=1)
  - [A tutorial on (Co)algebras and (Co)Induction](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.37.1418&rep=rep1&type=pdf)
- [Behavioural differential equations: a coinductive calculus of streams, automata, and power series](https://homepages.cwi.nl/~janr/papers/files-of-papers/tcs308.pdf)
- [Learning Automata with Side-Effects](https://discovery.ucl.ac.uk/id/eprint/10113536/1/camera-ready-11.pdf)
- [Runar Bjarnason's talk on machines](https://www.dropbox.com/s/jrq66rhzkmz4wft/Machines.pdf)
- [An approach to Object Semantics based on Terminal Co-Algebras](https://www.researchgate.net/publication/220173547_An_Approach_to_Object_Semantics_based_on_Terminal_Co-Algebras)
- [Many-sorted coalgebraic modal logic: a model theoretic study](http://www.numdam.org/article/ITA_2001__35_1_31_0.pdf)
- [Coalgebraic automata theory: basic results](https://arxiv.org/pdf/0811.1976.pdf)
- Very promising paper on dependently-typed interactive programs that introduces the concept of "weakly-final coalgebra": ["Interactive Programs and Weakly Final Coalgebras in Dependent Type Theory"](https://www.researchgate.net/publication/250396472_Interactive_Programs_and_Weakly_Final_Coalgebras_in_Dependent_Type_Theory)

### Operads

- [The Operad of Wiring Diagrams](https://arxiv.org/pdf/1305.0297.pdf)
- [Higher Algebra](http://people.math.harvard.edu/~lurie/papers/HA.pdf)
- [Higher Operads, Higher Categories](https://arxiv.org/pdf/math/0305049.pdf)
- [Cospans, Wiring Diagrams, and the Behavioral Approach](https://johncarlosbaez.wordpress.com/2015/05/05/cospans-wiring-diagrams-and-the-behavioral-approach/) (really, really good explanation of operads, much less obscure than the other papers linked)
- [Operadics - The Mathematics of Modular Design](http://www.appliedcategorytheory.org/wp-content/uploads/2017/09/Spivak-Operadics-The-mathematics-of-modular-design.pdf)
- [What is an Operad (math3ma blog)](https://www.math3ma.com/blog/what-is-an-operad-part-1) (as usual, best explanation of a tricky concept that I've encountered)

### Monoidal functors
Need to find some information about things that are between lax and strong monoidal functors: the coherence map for the opposite functor is a retraction/section for the coherence map of the functor, but they do not form a full isomorphism. Some promising search results:

- [Monoidal categories in, and linking, geometry and algebra](https://arxiv.org/pdf/1201.2991.pdf)
- [The problem with Lax Functors (see comments)](https://golem.ph.utexas.edu/category/2009/12/the_problem_with_lax_functors.html)

There's also some stuff about the interaction of applicatives and alternatives with monads (i.e. the functor composition monoidal structure) a lot of it by Mauro Jaskellioff:

- [A Unified View of Monadic and ApplicativeNon-determinism](https://www.fceia.unr.edu.ar/~mauro/pubs/UnifiedND.pdf)
- [From monoids to near semirings, the essence of `MonadPlus` and `Alternative`](https://usuarios.fceia.unr.edu.ar/~mauro/pubs/FromMonoidstoNearsemirings.pdf)

### Enrichment

My understanding of enrichment still needs a lot of work. I think a good path forward is to study:

1. [A 2-categories companion (some kind of course material explaining 2-categories and bicategories)](https://www.math.uchicago.edu/~may/IMA/Incoming/Lack/companion.pdf)
2. [Basic Bicategories (to understand the concept of a bicategory, a weakening of the definition of a 2-category)](https://arxiv.org/pdf/math/9810017.pdf)
3. ??? (maybe try and represent some monoids objects not in `(,)` as enriched single object categories, and study how monoidal functors interact with them)

### Relationship between (co)monads and monoidal structures
Almost everything by Tarmo Uustalu is relevant, esp. as relates to comonads

- [Lecture notes from a course "Containers for effects and contexts"](http://cs.ioc.ee/~tarmo/ssgep15/)
- [Programming Contextual Computations](https://www.cl.cam.ac.uk/techreports/UCAM-CL-TR-854.pdf)

### Brendan Fong
- http://www.brendanfong.com/
- [The Algebra of Open and Interconnected Systems](https://arxiv.org/pdf/1609.05382.pdf) - apparently there is some good stuff about hypergraphs in here

### Traced, compact (bi)categories

- The concept of a traced monoidal category is very interesting from the perspective of explaining recursion in programming. Related concepts in order of increasing generality are:
  - Trace
  - Traced-monoidal category
  - Compact category
  - Compact bicategory

- [Recursion from cyclic sharing](https://link.springer.com/chapter/10.1007/978-1-4471-0865-8_7)
- [Compact closed bicategories](https://arxiv.org/pdf/1301.1053.pdf) (very useful list of examples of compact bicategories in this one)
- [Monoidal bicategories and Hopf algebroids](https://pdf.sciencedirectassets.com/272585/1-s2.0-S0001870800X00680/1-s2.0-S0001870897916492/main.pdf?X-Amz-Security-Token=IQoJb3JpZ2luX2VjEAoaCXVzLWVhc3QtMSJIMEYCIQD3hTkSrAaNckb5kvK1WX9HKBbN2BZD4AJzZHI4BJh%2BtwIhALci3h1IhUMY%2BajPJkxC%2FYGpXUxv34R5Q0zYUBRx%2BoddKrQDCFMQAxoMMDU5MDAzNTQ2ODY1IgwYFnmvtYf8Uq1gdFoqkQPXKX%2FUTCNm%2BFZoG98gSPxEjaUO3AjhlJktAMo8RZBf1muU2DYBpNkYnS4MQxEwGo9fnbIGSmVE4knxJawCQnEy4sgCToGT5prP6Fpjpg6LNJ%2FF8NJMZkt7zlmhBH6zl1y8m4mwPuEs5yjAKQr3UiNuTPkz6Fmm%2BkfgQD3nWx8%2BTneoJHVs1HeodFeKdNKNI4UPwqWorcdozUTaN5vr7nMV3vlVFHtHZfcZNbSQXWToaWY7xaZl59rPxCqMxvjN7KPJbYh6t6JnzA4nnFlAAVviyI1Oi254EcU%2BPpvGHvzifTEZkITa4XDyB9awUgG7D%2BhrBflcuflmFJikcb9Cj6LmVFsDbAOiC7EpDKR0eD231e75WFcDF3IrrLTwOdKneuepjYjeZZ0HwG2hnjGPySe70A%2FHXP9z9rL3RHO0iTSY%2BQY3Rl4rJeb2IpuwfQBtSbnpI002AmxAQu%2Fpzme8FhpIUXmMLQJsnWDVja%2FM6t9wztMoa0ZRqK75q2R%2FVBrYSioFdjor%2F3ZApn3GrcJlgKRoEDCA64SDBjrqAS9ZyYkg7blDWlCjMXlMrLI6mxxr45KiYG%2FDns%2Fi9lKItgxZwBTaSxkeHGKcPTtUnXNkHdfqO61EeN94yeaW2LXXbwLc0zUP%2FkdsU2W1QNdeyJRDgF2O%2FE8BKFJtttItWhlDEQIhzDidLJQdTD%2Ft0Xh%2F%2FOcnwWevPrIFg0puPyR5X35MuLq2gwt36Aj%2BdcdCpOMqMWt4XlO5edB%2FWMUEXLdLxKBl3W184Pz%2BmJQrXVdDXC99Q6f%2FebjZugDS%2FvOtmlVqAvALFFZUQWPlSU0KLK%2B%2BUzBjIxsZkTTaXPXcbyhgPpbVdjHk5PjPKQ%3D%3D&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20210329T034716Z&X-Amz-SignedHeaders=host&X-Amz-Expires=300&X-Amz-Credential=ASIAQ3PHCVTYRFKRMMJF%2F20210329%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Signature=0f11ee96e32a49a096b05fd0c31ef00d1dd29ba73bedd4fa8b29410c6585ac53&hash=8ee93349e41722a1621a9f4140782a1730043fbf7ee7b7283def3f610c46aba5&host=68042c943591013ac2b2430a89b270f6af2c76d8dfd086a07176afe7c76c2c61&pii=S0001870897916492&tid=spdf-5e8106d4-7ba3-4866-afac-f21291f1bbc6&sid=b724a140324b16499099bec7094570ca3d45gxrqa&type=client)
- (only tangentially related in that it is mentioned as utilizing compact bicategories) [Polynomial functors and polynomial monads](https://arxiv.org/pdf/0906.4931.pdf)

### Retry logic, quantales, lattices

- I was looking at the retry library we use at work and I suspect that it can be radically simplified by equipping the (roughly) `data RetryAction = NoRetry | RetryASAP | RetryIn Int` data structure with a monoid data structure.
  - Andre Joyal's recent presentation on polynomial functors at the Topos Institute stream thing had a slide that got me interested in quantales. Specifically, `RetryAction` might represent a quantale, if we interpret `RetryIn Int` to be denoting the subset of the real line that is smaller than the specified upper bound. We can freely adjoin whatever monoid we want on `Int` so long as it distributes over the join.
  - Handy paper about using quantales to model "resource theories" (examples of resources modeled are very close to the exhaustible retry-tolerance we wish to model): [Quantitative Foundations for Resource Theories](https://drops.dagstuhl.de/opus/volltexte/2018/9699/pdf/LIPIcs-CSL-2018-32.pdf)
- [Quantales, Observational Logic and Process Semantics](https://citeseerx.ist.psu.edu/viewdoc/download;jsessionid=89840F29152C8E6D45C4B04BB90CEDD7?doi=10.1.1.210.1485&rep=rep1&type=pdf)
- [Whitman's solution to the word problem](https://bookstore.ams.org/surv-42/16) (for lattices, relevant for talking about the free lattice)
- [Free Lattices](https://math.hawaii.edu/~ralph/Classes/649M/freelat.pdf)

### Databases

- [Categorical Databases (introductory talk slides)](https://math.mit.edu/~dspivak/informatics/talks/CTDBIntroductoryTalk)

### Polynomial functors, monads (stuff from this is also scattered about elsewhere)

- [Topos Institute workshop on polynomial functors with lots of interesting presentations, specifically want to check out the ones on cofunctors and lenses](https://topos.site/p-func-2021-workshop/)

## Logic

### Ehrenfeucht–Fraïssé games

- http://www.math.toronto.edu/rossman/EFgames-lecture.pdf
- https://en.wikipedia.org/wiki/Ehrenfeucht%E2%80%93Fra%C3%AFss%C3%A9_game

## Computability

- [Categories and Computability](http://www.cs.ioc.ee/ewscs/2010/cockett/estonia-notes.pdf)
- [Platonism, Constructivisim, and Computer Proofs vs Proofs by Hand](https://pdfs.semanticscholar.org/8705/02fc88f3b1545146b535a8ddca9f8c45dcea.pdf)
- [Theoretical Computer Science for the Working Category Theorist](https://arxiv.org/pdf/1710.03090.pdf)

## Geometry

### Collision detection

I suspect that finding collisions between shapes (or convex hulls of shapes) has something to do with a lattice of shapes under inclusion as binary relation, intersection as meet, union as join.

- [On lattices of convex sets in R^n](https://arxiv.org/pdf/math/0409288.pdf)
- [On Proximity Problems in Open Spaces](https://curve.carleton.ca/system/files/etd/18d4b057-f42a-49e9-b943-ca43ee5cd76d/etd_pdf/ff64c38b3d8b80d6279ddf33bce507fc/barbaflores-onproximityproblemsineuclideanspaces.pdf)

The approach I was considering was to only admit circular subsets of points from a given canvas. Then the meet operation and join operation consists of picking a circle inscribed in the intersection of the two provided circles, and a circle just barely enclosing the two provided circles, respectively. Apparently the latter is a "closure operator", which taking convex hulls is also. The operation of taking the convex hull of the superposition of the provided shapes, when taken as the join operation, actually forms a proper join-semilattice. So maybe this wrapping circle business (or an adjustment of it) does too? Someone pointed out there might be problems with associativity.

Anyway here's a paper about closure operators and lattices:

- [Closure operators on sets and algebraic lattices](https://pdfs.semanticscholar.org/2fc9/320b490cfb8d759f6ec0fb9697434e6ddc78.pdf)

### Vector algebra

I want to render a game of life in toroidal coordinates on an actual torus. I started implementing my own vector algebra library using some generalized n-dimensional vector math stuff, but then became intrigued by what the generalization of the cross product to n-dimensions would be. Turns out this is called the Hodge Star operator. In the course of learning about this, I discovered a rabbithole of interesting things to read:

- [Course on discrete differential geometry](http://brickisland.net/DDGSpring2019/)
- [Wikipedia page on exterior algebra](https://en.wikipedia.org/wiki/Exterior_algebra)
- [TODO: fundamentals even on vector algebra are weak, find some nice resource on this]()
- [Wikipedia page on Hodge star operator](https://en.wikipedia.org/wiki/Hodge_star_operator)

Stuff I've played around with so far:

- [Implementation of game of life using traced comonad (traced probably works out really great for concatenating matrix transforms and doing relative coordinates in nD)](https://ywvr561j8z.codesandbox.io/)


## Graphs

I want to build a 3D git repo visualizer. Need to learn more about graph/tree layout algorithms esp in 3D:

- [Tree Drawing Algorithms and Tree Visualisation Methods (slides)](http://www.it.usyd.edu.au/~shhong/comp5048-lec2.pdf)
- [Cool hyperbolic geometry approach for rendering graphs using a spanning tree](https://graphics.stanford.edu/papers/h3cga/html/)
- [Algebraic Graphs with Class](https://eprint.ncl.ac.uk/file_store/production/239461/EF82F5FE-66E3-4F64-A1AC-A366D1961738.pdf)
- [Directed hypergraphs and applications](https://www.sciencedirect.com/science/article/pii/0166218X9390045P)
- [Algebra of parametrized graphs](https://pdfs.semanticscholar.org/fc44/cab864acb7e5ea07e04018d39f585e02d52c.pdf)

## Topology

@monoidmusician suggested https://mathoverflow.net/questions/19152/why-is-a-topology-made-up-of-open-sets as an entrypoint into topology stuff.

## Polyomino theory

I suspect that polyominos form a kind of colored operad. Specifically, the colors represent the "contour" of a polyomino-with-holes, and a morphism from a list of contours to a contour is a placement of the input contours such that they respect the boundaries of the output contour and do not overlap. Thus roughly speaking we can think of a multimorphism as a "tiling" of the output polyomino with the input polyominos.

Some fast and loose thinking shows that this appears to be:

- closed: given a valid tiling of a polyomino, and a valid tiling of each tile, there exists an obviously valid composition (i.e. that respects the contour of the outermost polyomino and avoids overlaps). the composition is roughly given by just deleting the contours of the intermediate tiles polyominos.
- unital: any polyomino contour P can simply be "tiled" with a single polyomino that occupies its entire surface. this is obviously a valid tiling, has domain [P] and codomain P. when postcomposed with any other tiling, it has no effect. when repeated to fill a list and precomposed with any other tiling, it also has no effect.
- associative: given a "three level" tiling of a polyomino, it does not matter in what order we forget about the two intermediate levels of contours.

Somewhat interestingly, no discussions appear to have occured on the category theory zulip about polyominos, and nlab also appears to be silent on the subject. Polyominos in general appear to be quite sparsely studied, and in particular their intersection with category theory appears to be completely unstudied.

EDIT: What I might be missing is that this is somehow equivalent to the little disks operad or some other operad of topological embeddings (although AFAIU topology isn't very interested in preventing continuous deformations, which we don't want here)?

"Tilings" seem to have some interesting intersections with  dynamic systems (which I'm currently studying from a coalgebraic perspective as part of my work on the cofree-bot stuff) and with algebraic topology and group theory. See for example:

- [Tilings, tiling spaces and topology](https://arxiv.org/pdf/math/0506054.pdf)

Also need to read more about [self-avoiding walks](https://en.wikipedia.org/wiki/Self-avoiding_walk), which are basically the contours of interest.

- [Lectures on self-avoiding walks](https://www.ihes.fr/~duminil/publi/saw_lecture_notes.pdf)
- [Lattice paths and random walks](https://www.stat.purdue.edu/~mdw/ChapterIntroductions/RandomWalksBousquetMelou.pdf)
- [Basic analytic combinatorics of directed lattice paths](https://www.sciencedirect.com/science/article/pii/S0304397502000075)

Some stuff on taxicab geometry that might generally be of use:

- [The generalized taxicab group](https://www.researchgate.net/publication/334173836_The_Generalized_Taxicab_Group) (also valuable as a survey containing lots of good references on taxicab geometry)

Power words: discrete geometry, algebraic topology, polytopes, packing, tiling, covering, incidence structure

# Music

- [Hearing Musical Streams](https://pdfs.semanticscholar.org/651c/a97da9f097e5e3b62cd859ca8396a4fe4f2a.pdf)

# Misc. blogs

- https://alexknvl.com
- https://coot.me/
- https://bartoszmilewski.com/
- https://adereth.github.io
  - https://adereth.github.io/blog/2015/02/02/poisonous-shapes/
