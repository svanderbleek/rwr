# rwr

the world's cutest javascript term rewriting system

Roadmap

- [ ] representations for expression, term
- [ ] rwr.rewrite(expression, rule) action
- [ ] rwr.logic rewrite logic, proofs in rewrite systems
- [ ] rwr.wolf mathematica interop
- [ ] rwr.redex racket redex implementation
- [ ] rwr.turnstile racket turnstile implementation
- [ ] rwr.webasm compile to webassembly?
- [ ] apply to rwr.lof by buidling self interpreting spartan

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



## Weird

* Fully Automated HTML and Javascript Rewriting for Constructing a Self-healing Web Proxy https://arxiv.org/pdf/1803.08725.pdf

## Quantifier Elimination

* Computation-Oriented Reductions of Predicate to Propositional Logic

## Unification

## Compiling

* An Architecture for Analysis https://sites.cs.ucsb.edu/~jmcmahan/research/top_picks_18.pdf

## Redex

* https://github.com/racket/redex

