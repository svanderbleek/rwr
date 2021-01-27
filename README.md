# rwrr

the internet's cutest javascript term rewriting system

Roadmap

- [ ] representations for expression, term
- [ ] rwrr.rewrite(expression, rule) action
- [ ] rwrr.logic rewrite logic, proofs in rewrite systems
- [ ] rwrr.wolf mathematica interop
- [ ] rwrr.redex racket redex implementation
- [ ] rwrr.turnstile racket turnstile implementation
- [ ] rwrr.webasm compile to webassembly?
- [ ] apply to rwrr.lof by buidling self interpreting spartan

## rwrr language

We will implement rwrr a javascript rewriting interpreter. The API is minimal.

```
match(expression, rule) 
rewrite(expression, rule)
evaluate(expression, environment)
```

It is inspired by mathematica and TRS presented in literature such as Term Rewriting Systems and Advanced Topics in Term Rewriting.

Rwrrr implements a rewriting logic and type checking ideas can be ported through this logic.

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

Expression

```
{Expression:{}}
```

Rewrite

```
replace({Expression1:{}}, {Expression1: {Expression2: {}}) == {Expression2:{}}
```

should implement what is needed for

* Simulation of Turing machines by a regular rewrite rule

theory

* Computing with Rewrite Systems https://core.ac.uk/download/pdf/82345385.pdf

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

