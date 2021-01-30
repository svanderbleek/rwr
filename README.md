# rwr

world's cutest javascript term rewriting system

Roadmap

- [ ] representations for expression, term
- [ ] rwr.rewrite(expression, rule) action
- [ ] rwr.logic rewrite logic, proofs in rewrite systems
- [ ] rwr.wolf mathematica interop
- [ ] rwr.redex racket redex implementation
- [ ] rwr.turnstile racket turnstile implementation
- [ ] rwr.webasm compile to webassembly?
- [ ] apply to rwr.lof by buidling self interpreting spartan

## Motivation 

* https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.35.9681&rep=rep1&type=pdf

* what the hell wolfy doin https://www.wolframphysics.org/technical-introduction/basic-form-of-models/basic-structure/

* apply to https://github.com/sicmutils/sicmutils

* https://github.com/mhuebert/maria
* https://docs.racket-lang.org/quick/

* http://www.cs.tau.ac.il/~nachum/papers/taste-fixed.pdf

> Rewrite systems have long been used as decision procedures for validity in equational theories, that is,
for truth of an equation in all models of the theory.

## Unification

* https://github.com/bramstein/junify/blob/master/lib/unification.js

## TRS

* lectures https://web.archive.org/web/20180308210524/https://www.cs.vu.nl/~tcs/trs/
* thue https://github.com/catseye/Thue
* markov algorithm https://esolangs.org/wiki/Markov_algorithm
* refal http://www.math.bas.bg/bantchev/place/refal.html
* snobol http://www.math.bas.bg/bantchev/place/snobol.html
* pure https://agraef.github.io/pure-lang/
* https://www.stephendiehl.com/posts/exotic02.html
* maude http://maude.lcc.uma.es/maude31-manual-html/maude-manual.html
* egison

## Examples

* from http://aprove.informatik.rwth-aachen.de/help_new/trs.html

```
Simple Example
      (VAR x y)
      (RULES

        plus(s(s(x)),y) -> s(plus(x,s(y)))
        plus(x,s(s(y))) -> s(plus(s(x),y))
        plus(s(0),y) -> s(y)
        plus(0,y) -> y

        ack(0,y) -> s(y)
        ack(s(x),0) -> ack(x,s(0))
        ack(s(x),s(y)) -> ack(x,plus(y,ack(s(x),y)))
      )
Context Sensitive Example
      (VAR X Y Z)
      (STRATEGY CONTEXTSENSITIVE
        (and 1)
        (true)
        (false)
        (if 1)
        (add 1)
        (0)
        (s)
        (first 1 2)
        (nil)
        (cons)
        (from)
      )
      (RULES
      and(true,X) -> X
      and(false,Y) -> false
      if(true,X,Y) -> X
      if(false,X,Y) -> Y
      add(0,X) -> X
      add(s(X),Y) -> s(add(X,Y))
      first(0,X) -> nil
      first(s(X),cons(Y,Z)) -> cons(Y,first(X,Z))
      from(X) -> cons(X,from(s(X)))
      )
Equational Example
      (VAR x y u v w)

      (RULES
        minus(plus(x, y), y) -> x
        div(0, plus(y, 1)) -> 0
        div(plus(x, 1),plus(y, 1)) -> plus(div(minus(x, y), plus(y, 1)), 1)
      )
      (THEORY (EQUATIONS
        plus(0, 0) == 0
        plus(1, 0) == 1
        plus(0, 1) == 1
        plus(u, plus(v, w)) == plus(plus(u, v), w)
      ))
AC Example
      (VAR x y)
      (THEORY (AC plus))
      (RULES
        plus(x, 0) -> x
        plus(x, s(y)) -> s(plus(x, y))
      )
```

## Termination

* http://aprove.informatik.rwth-aachen.de/
* Mechanizing and Improving Dependency Pairs http://citeseerx.ist.psu.edu/viewdoc/download;jsessionid=32F81BEA61AC7E7E5B3B261650ACB70A?doi=10.1.1.103.302&rep=rep1&type=pdf

## editor

* https://www.maria.cloud/quickstart
* https://www.unisonweb.org/2020/03/12/march-update/

## rwr language

ee will implement rwr a javascript rewriting interpreter. The API is minimal.

```
match(expression, rule) 
rewrite(expression, rule)
evaluate(expression, environment)
```

It is inspired by mathematica and TRS presented in literature such as Term Rewriting Systems and Advanced Topics in Term Rewriting.

rwr implements a rewriting logic and type checking ideas can be ported through this logic.

## Impelmentations

* http://www.jaist.ac.jp/~hirokawa/tool/

## Thoerem Proving

* Term rewriting and beyond — theorem proving in Isabelle

## Rewriting

* javascript term rewriting https://github.com/fbreuer/rewritr
* Algebra in my browser https://www.youtube.com/watch?v=S2OEPFbsl50

```
ReplaceAll [Object, [Rules]]
```

* lisp mathematica https://dl.acm.org/doi/abs/10.1145/1089419.1089421?download=true
* matematica evaluation https://reference.wolfram.com/language/tutorial/EvaluationOfExpressionsOverview.html

we use a close version:

```
["f" ["x"]]
```

* Simulation of Turing machines by a regular rewrite rule

theory

* Computing with Rewrite Systems https://core.ac.uk/download/pdf/82345385.pdf

## Parser

* Adaptive parser https://github.com/jarble/adaptive_parser

## JavaScript metatheory

* mechanized metatheory for the mases https://repository.upenn.edu/cgi/viewcontent.cgi?article=1248&context=cis_papers
* closure calculus? https://dl.acm.org/doi/10.1145/3294032.3294085
* binders and alpha for free?

## Quantifier Elimination

* Computation-Oriented Reductions of Predicate to Propositional Logic

## Unification

## Compiling

* An Architecture for Analysis https://sites.cs.ucsb.edu/~jmcmahan/research/top_picks_18.pdf

## Redex

* https://github.com/racket/redex

## Weird

* Fully Automated HTML and Javascript Rewriting for Constructing a Self-healing Web Proxy https://arxiv.org/pdf/1803.08725.pdf


