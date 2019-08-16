---
title: A Nearly Pointless Reconstruction of the Real Numbers
subtitle: And why it's important for quantum mechanics.
date: 2019-08-14
tags: [physics, math, quantum mechanics]
---

OK, I need to write this stuff out for the sake of my own understanding. Please excuse my (mathematically formal) language. 

# Conceptual Motivation

## The problem with exact measurement
Typically we think of measurement as assigning a real number to a real-world phenomenon. Thus, a measurement function is a [surjection](https://en.wikipedia.org/wiki/Surjective_function) from the set of observable states onto (an interval of) $$\mathbb{R}$$. However, this isn't really how it works. [Almost all](https://en.wikipedia.org/wiki/Almost_all) real numbers are non-[computable](https://en.wikipedia.org/wiki/Computable_number), so almost all possible measurement outcomes cannot be specified in a finite number of steps, nor can it be completed in finite time. Indeed, we have it even worse than this because even if (in some measurement basis) a real-world observable $$x$$ takes a value from the computable numbers (a rational value, for example), this cannot be determined in finite time. It would still take an infinite number of steps to unambiguously distinguish the value of $$x$$ from the (uncountably many) other real numbers arbitrarily close to $$x$$.

In more familiar terms, if we want to write down an arbitrary real number in decimal notation *exactly*, we have to write down *all* of its digits. This, of course, cannot be done in finite time. Thus, if we want to measure some real-world quantity *exactly*, such as the distance between to points, we have to determine *all* of the significant digits of the measurement. Even if the quantity has some "nice" value -- $$2$$ cm, for example -- to unambiguously determine this, we still have to determine all of it's significant digits. Otherwise, how do we know that the true value isn't, say, $$2.0000000000000000143052\dots$$ cm or $$1.999999999999999919167\dots$$ cm? One might be tempted to say, "Well at some point we get to lengths smaller than the proton, or even the [Planck length](https://en.wikipedia.org/wiki/Planck_length). So obviously we can't be more precise than that." But that's getting ahead of ourselves. The point is to study measurement in a purely mathematical context and see how it leads us to the rules of quantum mechanics.

The takeaway here is that all measurements necessarily have finite precision. This is not, as one might suppose, simply due to our imperfect instruments or (as way too many undergraduate students say in their lab reports) "human error." *It is an inherent property of the real numbers*. Or, more precisely, an inherent property of the set of continuous functions onto $$\mathbb{R}$$. In other words, "perfect" instruments are a ([measure](http://mathworld.wolfram.com/MeasureTheory.html)) theoretical impossibility.

The best we can do when making a measurement -- indeed, what we actually do whenever we make a measurement -- is to specify an open interval, $$S$$, that (we imagine) contains the "true" value. The measure of this interval is bounded below by our "smallest possible measurement": $$\mu(S) \ge \delta$$ for some specific $$\delta \in \mathbb{Q}$$ which depends on our measurement method. 

## The problem of the measurement basis
Since there is no universal, "God given" coordinate system, whenever we make a measurement, we have to establish a measurement basis. That is, we must pick a few points to measure in reference to. Specifically, if the measurement can take values from $$\mathbb{R}$$, then we need two points which we could label $$0$$ and $$1$$, the origin and the point one (positive) unit from the origin. From this we could measure any distance along the line passing through $$0$$ and $$1$$.

However, if we look closely, we notice a serious problem. We can't just pick two points in empty space. How would we clearly specify them? We need real-world observables to anchor these points to. We need an actual stick to use as a ruler. But as before, we can't know exactly where our base points are. We can't know exactly how long our ruler is. As before, the best we can do is to specify open neighborhoods and say "$$0$$ is in here and $$1$$ is in there."

## The plan
This is my first draft of working all of this out on paper. Hopefully, if done right, this construction will make it clear why measurements are inherently probabilistic and why the [Born rule](https://en.wikipedia.org/wiki/Born_rule) is the way to represent states and observables. Hopefully I may also be able to show why states evolve according to the Schrödinger equation, and what constitutes an observation for the purposes of "snapping into" an eigenstate. (Hint: it has nothing to do with human minds).

# The Pointless Order Topology
I started writing this section and got myself so turned around that I had to pretty much scrap everything and start over.

In all of the following, declared sets (represented with a single character) will be understood to be inhabited unless otherwise stated. This assumption will not necessarily extend to sets defined by relations (such as intersection).

Let $$\mathcal{T}$$ be a collection of open sets of some set $$X$$ with two [partial orders](http://mathworld.wolfram.com/PartialOrder.html) defined on them, 
- **Inclusion:** $$\subseteq$$
- **Scalar ordering:** $$\le$$

with the following properties:
1. $$(\mathcal{T},\subseteq)$$ is a (generalized) topology.  
2. $$\le$$ is a total order on any collection of pairwise disjoint sets. That is, if $$A \cap B = \varnothing$$ then either $$A < B$$ or $$B < A$$. The empty set is not comparable to any inhabited set.

**Definition:** A set $$B$$ to be *bounded* if there exists sets $$A$$ and $$C$$ such that $$A<B<C$$. Call $$A$$ a *lower bound* for $$B$$ and $$C$$ an *upper bound* for $$B$$. 

**Definition:** A collection of sets $$B_i$$ to be bounded if 

$$\exists A, C$$ s.t. $$\forall i, \: A<B_i<C$$.

**Definition:** A collection of sets is *locally finite*

3. Let $$\mathcal{B}$$ be a countable collection of sets with the property that 

$$\forall A \in \mathcal{T}$$ either $$A \cap B = B$$ or $$A \cap B = \varnothing$$.

That is, $$\mathcal{B}$$ is the set of smallest inhabited sets. Clearly distinct $$B$$ are pairwise disjoint. Also, it follows directly from their definitions that $$\mathcal{B}$$ is a topological base for $$\mathcal{T}$$ and that each $$B \in \mathcal{B}$$ is the principal set for an ultrafilter. Furthermore, let $$\mathcal{B}$$ be locally finite in the sense that any bounded collection

# The Algebraic Structure

# The Measure


> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTAwNzk1MDI1MSw1ODk2NzczNDIsMTQ1OT
YwNDM2MiwtMjAyMjA5OTM3Nyw5NzA4NDYxNTQsLTE1MjE4Njcw
MDIsODM0MjQyODkxLC01NDQ5MTU2ODQsLTE2MjA2NzA3NDgsLT
I2MjA1OTEwMSwtMTIxMzA2MjY0NSwtMTI1MDE4OTI0NywtMTYz
MzQyNDE1OCwtNDcyMzgzMzU1LDEwNjYxNzU3MDksLTg4MDkwNj
U1NiwxODU4ODc1NDE4LDEzMTk5MjE2OSwtNTMxNjAxNzI2LC0x
NDA3MDE2MjAzXX0=
-->