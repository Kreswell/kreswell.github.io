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

---
Let $$X$$ be a space. We're going to construct several different structures on $$X$$. Two of these are order structures, so we need to be careful with notation to avoid confusion. The goal is for $$X$$ to look like $$\mathbb{R}$$, but with some restrictions on what we can and cannot know.
1. $$X$$ is a set, so it contains a nonzero number of elements.
2. We can specify proper subsets of $$X$$ (and proper subsets of those).
3. The usual set relations of inclusion, union, and intersection are well-defined.
4. The empty set, $$\varnothing$$ exists.
5. We can tell if a set is inhabited (contains a nonzero number of elements), and we can tell if a set is empty (contains zero elements).

However,

6. We cannot make logical statements about set elements directly. At best, we can make universal ("for all") statements about elements based on which sets they inhabit.

As we will see, there will be some "unexcluded middle" statements. For example, there may exist sets where we can't tell whether or not they are inhabited.

# The Pointless Topology
For brevity, it will be assumed that all declared sets are inhabited. This assumption does not necessarily extend to sets defined via relations on declared sets.

Let $$\mathcal{T}$$ be a collection of subsets of $$X$$ with the following properties:
1. $$\mathcal{T}$$ is a topology. That is:
  - $$X \in \mathcal{T}$$
  - $$\varnothing \in \mathcal{T}$$
  - $$\forall A,B \in \mathcal{T}, A \cap B \in \mathcal{T} $$
  - $$\forall A_i \in \mathcal{T}, \bigcup_i A_i \in \mathcal{T} $$
2. Proper set inclusion is defined by:
$$A \subset C$$ iff $$A \subseteq C$$ and $$\exist B \subseteq C$$

# The Linear Order

# The Algebraic Structure

# The Measure


> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbOTM4NjEzNTU4LC04Nzk1Njc3MTQsMTk4OT
I2ODE1NSwxNzk2Njc5MDgxLC0xODQ3MTkzMDM5LDgzOTYzMTM2
LC0xODM3Nzk3MTE2LDEyNzU1MjA2ODhdfQ==
-->