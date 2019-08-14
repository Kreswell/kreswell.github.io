OK, I need to write this stuff out for the sake of my own understanding. Please excuse my (mathematically formal) language. 

# A Pointless Reconstruction of the Real Numbers
Let $X$ be a space. We're going to construct several different structures on $X$. Two of these are order structures, so we need to be careful with notation to avoid confusion.

## Conceptual Motivation
Typically we think of measurement as assigning a real number to a real-world phenomenon. Thus, a measurement function is a [surjection](https://en.wikipedia.org/wiki/Surjective_function) from the set of observable states onto (an interval of) $\mathbb{R}$. However, this isn't really how it works. [Almost all](https://en.wikipedia.org/wiki/Almost_all) real numbers are non-[computable](https://en.wikipedia.org/wiki/Computable_number), so almost all possible measurement outcomes cannot be specified in a finite number of steps, nor can it be completed in finite time. Indeed, we have it even worse than this because even if (in some measurement basis) a real-world observable $x$ takes a value from the computable numbers (a rational value, for example), this cannot be determined in finite time. It would still take an infinite number of steps to unambiguously distinguish the value of $x$ from the (uncountably many) other real numbers arbitrarily close to $x$.

In more familiar terms, if we want to write down an arbitrary real number in decimal notation *exactly*, we have to write down *all* of its digits. This, of course, cannot be done in finite time. Thus, if we want to measure some real-world quantity *exactly*, such as the distance between to points, we have to determine *all* of the significant digits of the measurement. Even if the quantity has some "nice" value -- $2$ cm, for example -- to unambiguously determine this, we still have to determine all of it's significant digits. Otherwise, how do we know that the true value isn't, say, $2.0000000000000000143052\dots$ cm or $1.999999999999999919167\dots$ cm? One might be tempted to say, "Well at some point we get to lengths smaller than the proton, or even the [Planck length](https://en.wikipedia.org/wiki/Planck_length). So obviously we can't be more precise than that." But that's getting ahead of ourselves. The point is to study measurement in a purely mathematical context and see how it leads us to the rules of quantum mechanics.

The takeaway here is that all measurements necessarily have finite precision. This is not, as one might suppose, simply due to our imperfect instruments or (as way too many undergraduate students say in their lab reports) "human error." *It is an inherent property of the real numbers*. Or, more precisely, an inherent property of the space of continuous functions onto $\mathbb{R}$.

## The Pointless Topology

## The Linear Order

## The Algebraic Structure

## The Measure


> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTc3MDgzNDU4NywtMTE1MTk4NTMzMiwtNj
MzOTA0OTQ2LDk4Mzg0NDUxOSw4MzUwMzY2ODYsOTU4NTg0ODU3
LC0xOTA3ODkyNjA0LDI5NTc4MzU1OSwxNzAyMTQ2NTcwXX0=
-->