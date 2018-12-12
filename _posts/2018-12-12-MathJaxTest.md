---
layout: post
title: MathJax Test
subtitle: Can I MathJax and have it properly format LaTeX markup?
tags: [test]
---

# First Test

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

# Second Test

Hmmm... it seems to handle [double dollar](https://trigun.fandom.com/wiki/Chapter_1) signs fine in markdown and html, although it seemed to treat it as inline math in markdown. Let's just test that a few more times: $$ x = \frac{-b \pm \sqrt{(b^2 - 4ac)}}{2a} $$, $$ \sum_{n=0}^{\infty}\frac{1}{2^n} = 2 $$, $$ \nabla \cdot \mathbf{E} &= \frac{\rho}{\varepsilon_0} $$.

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
