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

The reason why, is that we can "squeeze" down to it with rational numbers. To make it really clear what we're doing, I'm going to work in explicit fractions. Let's make a list of the squares of some rational numbers to try to home-in on $\sqrt{2}$.

$$
	\begin{array}{cll}
	1^2 &= 1 &\text{Too small.} \\
	2^2 &= 4 &\text{Too big.} \\
	\left(\frac{3}{2}\right)^2 &= \frac{9}{4} = 2.25 &\text{Closer, but still too big.} \\
	\left(\frac{4}{3}\right)^2 &= \frac{16}{9} = 1.777\dots &\text{Too small.} \\
	\left(\frac{5}{3}\right)^2 &= \frac{25}{9} = 2.777\dots &\text{Too big.} \\
	\left(\frac{5}{4}\right)^2 &=\frac{25}{16} = 1.5625 &\text{Too small.} \\
	\left(\frac{7}{5}\right)^2 &=\frac{49}{25} = 1.96 &\text{Getting closer...} \\
	\left(\frac{8}{5}\right)^2 &=\frac{64}{25} = 2.56 &\text{Too big.} \\
	\vdots & & \vdots
	\end{array}
$$

So what's so different about $\sqrt{-1}$? We're still inventing a new number to solve the equation

$$
	x^2 = n,
$$

but now we can't over/under-shoot the estimate with rational numbers. There are no rational numbers that square to a negative number. *That's* what's so weird about "imaginary" numbers. There's no $n \in \mathbb{Q}$ such that $n^2$ is "close" to -1. So instead, we just give $\sqrt{-1}$ a name, $i$, and call it a new thing. Remember, inventing a new number is not a new activity! As [Leopold Kroeneker said]([https://en.wikipedia.org/wiki/Leopold_Kronecker](https://en.wikipedia.org/wiki/Leopold_Kronecker)), (paraphrased) we "start" with the integers -- really the natural numbers -- and invent thre rest. We invented rational numbers to solve problems involving the inverse of multiplication, and we invented the real numbers -- actually the *algebraic* numbers -- to invert exponentiation by integers. So it's not so weird to invent new numbers to solve 

$$
x^2 = n
$$

for $n \in -\mathbb{N}$.

Now you may be wondering, "That argument sounds good, but these numbers don't fit anywhere on the real line. So what do we do with them?" Well, 

 
> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMzk1NTM2NTksMjEyNjMyNzc5N119
-->