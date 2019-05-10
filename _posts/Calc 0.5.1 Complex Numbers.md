---
layout: post
title: Calc 0.5.1 Complex Numbers
subtitle: The reality of imaginary numbers
date: 2019-05-10
tags: [math]
---

Complex numbers have a reputation of being *bizarre* or *other-worldly*. I blame the name. I mean, if you call $\sqrt{-1}$ the *imaginary* unit, then of course people are going to think of it as belonging to some kind of weird fantasy realm of mathematics. When, really, $\sqrt{-1}$ is no less bizarre than $\sqrt{2}$.  

Let's think about $\sqrt{2}$, or as I prefer to say (the *better* way of writing it), $2^{\frac{1}{2}}$. The algebra problem

$$
	x^2 = n
$$

has a nice solution for $n \in \{0,1,4,9,16,\dots\}$. But for other values of $n \in \mathbb{N}$, we don't have obvious answers. We have to *invent* new numbers to solve the equation. Historically (at least apocryphally), it was surprising that $\sqrt{2}$ is not rational. But to me, it's a little suspect that we can call it a number at all. Why is $\sqrt{2}$ even a reasonable thing to write down? 

The reason why, is that we can "squeeze" down to it with rational numbers. To make it really clear what we're doing, I'm going to work in explicit fractions, rather than decimal representation. Let's make a list of the squares of some rational numbers to try to home-in on $\sqrt{2}$.

$$
	\begin{tabular}
		1^2 &= 1 \qquad \text{Too small.}\\
		2^2 &= 4 \qquad\qquad\qquad\qquad \text{Too big.} \\
	\left(\frac{3}{2}\right)^2 &= \frac{9}{4} = 2.25 \qquad\qquad \text{Closer, but still too big.} \\
	\left(\frac{4}{3}\right)^2 &= \frac{16}{9} = 1.777\dots \qquad \text{Too small.} \\
	\left(\frac{5}{3}\right)^2 &= \frac{25}{9} = 2.777\dots \qquad \text{Too big.}
	\end{aligned}
$$

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTIxMzE3Mjc5MjYsMjEyNjMyNzc5N119
-->