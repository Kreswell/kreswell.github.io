---
layout: post
title: MathJax Test
subtitle: Can I MathJax and have it properly format LaTeX markup?
tags: [test]
---

# Figuring out the syntax

## First Test
The first test is to include the MathJax script call in the head.html file, which I've done. Let's test a few things.
1. Inline math with `\( ... \)`: \( \LaTeX \), \( \hbar = 1.0545718\times 10^{-34}\: kg\cdot m^2/s \), \( x = \frac{-b \pm \sqrt{(b^2 - 4ac)}}{2a} \).
2. Inline math with `$ ... $`: $\LaTeX$, $\hbar = 1.0545718\times 10^{-34}\: kg\cdot m^2/s$, $x = \frac{-b \pm \sqrt{(b^2 - 4ac)}}{2a}$.
3. Display math with `\[ ... \]`:
\[ x = \frac{-b \pm \sqrt{(b^2 - 4ac)}}{2a} \]
4. Display math with `$$ ... $$`:
$$ x = \frac{-b \pm \sqrt{(b^2 - 4ac)}}{2a} $$

Next let's try including it inside html (in this case, a `<ol></ol>` block):
<ol>
  <li>
    Inline math with <code>\( ... \)</code>: \(\LaTeX\), \(\hbar = 1.0545718\times 10^{-34}\: kg\cdot m^2/s\), \(x = \frac{-b \pm \sqrt{(b^2 - 4ac)}}{2a}\).
  </li>
  <li>
    Inline math with <code>$ ... $</code>: $\LaTeX$, $\hbar = 1.0545718\times 10^{-34}\: kg\cdot m^2/s$, $x = \frac{-b \pm \sqrt{(b^2 - 4ac)}}{2a}$.
  </li>
  <li>
    Display math with <code>\[ ... \]</code>:
    <br>
    \[ x = \frac{-b \pm \sqrt{(b^2 - 4ac)}}{2a} \]
  </li>
  <li>
    Display math with <code>$$ ... $$</code>:
    <br>
    $$ x = \frac{-b \pm \sqrt{(b^2 - 4ac)}}{2a} $$
  </li>
</ol>

If this doesn't work, the next thing to try is including the `<script></script>` line in this .md file itself, although I'm not sure if I need to include it inside a `<head></head>` block.

## Second Test
Hmmm... it seems to handle [double dollar](https://trigun.fandom.com/wiki/Chapter_1) signs fine in markdown and html, although it seemed to treat it as inline math in markdown. Let's just test that a few more times: $$ x = \frac{-b \pm \sqrt{(b^2 - 4ac)}}{2a} $$, $$ \sum_{n=0}^{\infty}\frac{1}{2^n} = 2 $$, $$ \nabla \cdot \mathbf{E} = \frac{\rho}{\varepsilon_0} $$.

I think it treated the backslash as an escape character, at least in some contexts, and so didn't interpret them as $$\LaTeX$$ blocks. Let's see what it does with double backslash: \\( x = \frac{-b \pm \sqrt{(b^2 - 4ac)}}{2a} \\), \\( \hbar = 1.0545718\times 10^{-34}\: kg\cdot m^2/s \\).

Perhaps it will produce display math with nested delimeters - `$$ \[ ... \] $$`. Let's try it. Here are a few equations with different line breaks (just to see if that matters):

$$\[ x = \frac{-b \pm \sqrt{(b^2 - 4ac)}}{2a} \]$$

$$ \[
  x = \frac{-b \pm \sqrt{(b^2 - 4ac)}}{2a}
\] $$

$$
\[
  x = \frac{-b \pm \sqrt{(b^2 - 4ac)}}{2a}
\]
$$

And one with double backslash plus square brackets - `\\[ ... \\]`:
\\[ x = \frac{-b \pm \sqrt{(b^2 - 4ac)}}{2a} \\]

## Results
It looks like there are two approaches that will work: double dollar signs or double backslashes. I think that double dollar signs produce inline math if it's not preceded by a line break, and display math if it is. Let's double-check that. Here's an equation with no line breaks before or after: $$ x = \frac{-b \pm \sqrt{(b^2 - 4ac)}}{2a} $$, here's the same equation with a single line break both before and after:
$$ x = \frac{-b \pm \sqrt{(b^2 - 4ac)}}{2a} $$
Here's the same one with a double line break both before and after:

$$ x = \frac{-b \pm \sqrt{(b^2 - 4ac)}}{2a} $$

Here's the same one with no line break before and a single one after. $$ x = \frac{-b \pm \sqrt{(b^2 - 4ac)}}{2a} $$
And here's one with a double line break before

$$ x = \frac{-b \pm \sqrt{(b^2 - 4ac)}}{2a} $$ and no line break after.

So it appears there needs to be a double-space before and after a `$$ ... $$` block to be display style, otherwise it's inline style.

This is great! I can easily type equations in markdown and have it look great on the final page.

## Further tests
Let's test a bunch more stuff. 

### Inline $$\LaTeX$$ formatting in section headings

### Syntax highlighting in code blocks.

```latex
\begin{equation}
  x = \frac{-b \pm \sqrt{(b^2 - 4ac)}}{2a}
\end{equation}
```

### Numbered (maybe?) equations

Here's how it renders the above code block:

$$
\begin{equation}
  x = \frac{-b \pm \sqrt{(b^2 - 4ac)}}{2a}
\end{equation}
$$

### Multi-line equation blocks (aka. Does it use the 'mathtools' or 'amsmath' package?)

Here's how it displays

```latex
\begin{aligned}
  \nabla \cdot \mathbf{E} &= \frac{\rho}{\varepsilon_0} \\
  \nabla \cdot \mathbf{B} &= 0 \\
  \nabla \times \mathbf{E} &= -\frac{\partial \mathbf{B}}{\partial t} \\
  \nabla \times \mathbf{B} &= \mu_0\left(\mathbf{J}+\varepsilon_0\frac{\partial \mathbf{E}}{\partial t}\right)
\end{aligned}
```

$$
\begin{aligned}
  \nabla \cdot \mathbf{E} &= \frac{\rho}{\varepsilon_0} \\
  \nabla \cdot \mathbf{B} &= 0 \\
  \nabla \times \mathbf{E} &= -\frac{\partial \mathbf{B}}{\partial t} \\
  \nabla \times \mathbf{B} &= \mu_0\left(\mathbf{J}+\varepsilon_0\frac{\partial \mathbf{E}}{\partial t}\right)
\end{aligned}
$$

### Matrices

Here's how it renders

```latex
A = 
\begin{bmatrix}
    a_{11} & a_{12} & a_{13} \\
    a_{21} & a_{22} & a_{23} \\
    a_{31} & a_{32} & a_{33} \\
\end{bmatrix}
```
$$
A = 
\begin{bmatrix}
    a_{11} & a_{12} & a_{13} \\
    a_{21} & a_{22} & a_{23} \\
    a_{31} & a_{32} & a_{33} \\
\end{bmatrix}
$$

If this all works, it would appear that it works basically the same as in a Jupyter notebook. I wonder if Jupyter uses MathJax. It probably does. (And I'm sure I could find out if I wanted to bother looking it up.)
