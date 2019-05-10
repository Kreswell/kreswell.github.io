---
layout: post
title: StackEdit Test
subtitle: Testing publishing directly from StackEdit
date: 2019-05-10
tags: [test]
---

# StackEdit Test
I recently discovered StackEdit as a really user-friendly, web-based editor for Markdown documents with $$\LaTeX$$-ish[<sup>1</sup>](#1) support. It has an option to publish documents to various sites, including GitHub, Blogger, and WordPress. I've created accounts on all of those sites in the process of trying to find my favorite way to write blog posts. This is a test document to see what happens to the formatting when I publish to those sites.

## Some test math
The Jacobian matrix $$J$$ of a multi-variable function $$f : \mathbb{R}^n \mapsto \mathbb{R}^n$$ can be written as
$$
	J = 
	\begin{bmatrix}
		\frac{\partial f_1}{\partial x_1} & \frac{\partial f_1}{\partial x_2} & \cdots & \frac{\partial f_1}{\partial x_n} \\
		\frac{\partial f_2}{\partial x_1} & \frac{\partial f_2}{\partial x_2} & \cdots & \frac{\partial f_2}{\partial x_n} \\
		\vdots & \vdots & \ddots & \vdots \\
		\frac{\partial f_n}{\partial x_1} & \frac{\partial f_n}{\partial x_2} & \cdots & \frac{\partial f_n}{\partial x_n}
	\end{bmatrix}
$$
And here's the code I typed:
```latex
$$
	J = 
	\begin{bmatrix}
		\frac{\partial f_1}{\partial x_1} & \frac{\partial f_1}{\partial x_2} & \cdots & \frac{\partial f_1}{\partial x_n} \\
		\frac{\partial f_2}{\partial x_1} & \frac{\partial f_2}{\partial x_2} & \cdots & \frac{\partial f_2}{\partial x_n} \\
		\vdots & \vdots & \ddots & \vdots \\
		\frac{\partial f_n}{\partial x_1} & \frac{\partial f_n}{\partial x_2} & \cdots & \frac{\partial f_n}{\partial x_n}
	\end{bmatrix}
$$
```
That was a bit of overkill with all the `\cdots`, `\vdots`, and `\ddots`, but I wanted to see how they looked. As a test of multi-line equations, let's try Maxwell's equations. 
$$
	\begin{aligned}
	\nabla \cdot \mathbf{E} &= \frac{\rho}{\epsilon_0} \\
	\nabla \cdot \mathbf{B} &= 0 \\
	\nabla \times \mathbf{E} &= -\frac{\partial \mathbf{B}}{\partial t} \\
	\nabla \times \mathbf{B} &= \mu_0 \left( \epsilon_0\frac{\partial \mathbf{E}}{\partial t} + \mathbf{J} \right)
	\end{aligned}
$$

This works in the editor, but I have to use `\begin{aligned}` and `\end{aligned}` (unlike MathJax, which just knows to do aligned lines if you use the `&` and `\\`. I still haven't figured out how to do equation numbers yet.

Let's publish it to different places and see how it looks.

---
###### 1 
It uses KaTeX rather than MathJax, like a lot of Markdown editors. I haven't noticed much difference yet.


> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMjE2MjQxNDQzLDEzNDg4OTk2MjcsMjE2Mj
QxNDQzXX0=
-->